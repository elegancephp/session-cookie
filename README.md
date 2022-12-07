# elegance/session-cookie

Controla sessão e cookies do PHP

    composer require elegance/session-cookie
---

### [Documentação](https://github.com/elegancephp/session-cookie/tree/main/.doc)

 - [helper](https://github.com/elegancephp/session-cookie/tree/main/.doc/helper)
    - [config](https://github.com/elegancephp/session-cookie/tree/main/.doc/helper/config.md)
 
---

### Sessão

    use Elegance\Session;

A variavel de ambiente **SESSION_TIME** determina o tempo de vida da sessão em horas. O padrão é 24

> Variaveis de sessão com nome iniciado em **#** serão tratadas como **FLASH** (podem ser recuperadas apenas uma vez)

**check**
Verifica se uma variavel de sessão existe ou se tem um valor igual ao fornecido

    Session::check(string $name): bool

**set**
Define um valor para uma variavel de sessão

    Session::set(string $name, mixed $value = null): void

**get**
Retorna o valor de uma variavel de sessão

    Session::get(string $name): mixed

**remove**
Remove uma variavel de sessão

    Session::remove(string $name): void

---
### Cookie

    use Elegance\Cookie;

A variavel de ambiente **COOKIE_TIME** determina o tempo de vida dos cookies em horas. Por padrão, utiliza-se o valor de **SESSION_TIME**

> Definir a variavel de ambiente **COOKIE_TIME** como **0**, faz com os cookies sejam excluidos quando o navegador for fechado

> Cookies com nome iniciado em **#** terão seus nomes codificados e seus valores cifrados

**check**
Verifica se um cookie existe ou se tem um valor igual ao fornecido

    Cookie::check(string $name): bool

**set**
Define um valor para um cookie

    Cookie::set(string $name, mixed $value = null): void

**get**
Retorna o valor de um cookie

    Cookie::get(string $name): mixed

**remove**
Remove um cookie

    Cookie::remove(string $name): void