# Culqi Go 


[![License](https://poser.pugx.org/culqi/culqi-php/license)](https://packagist.org/packages/culqi/culqi-php) 

http://shields.io/

![](https://raw.githubusercontent.com/zeit/art/5824d39f6b3f714c51d40e8cdc4cb2673142527a/release/repo-banner.png)


Biblioteca de CULQI para el lenguaje Go (golang), pagos simples en tu sitio web. Consume el Culqi API.

| Versión actual| Culqi API|
|----|----|
| 0.1.0 (09-01-2017) |v2 (ir a referencia)|



## Requisitos 

- Go 1.6+ 
- Credenciales de comercio en Culqi (1).

## Instalación 


### Vía "go get"


```bash
go get -u github.com/brayancruces/go-lang
```


### Manualmente

Clonar el repositorio o descargarse el código fuente.

```bash
$ git clone git@github.com:brayancruces/culqi-golang.git
```

## Inicio rápido 

Antes de comenzar a utilizar la biblioteca, inicialmente hay que configurar las credenciales del comercio (Código de Comercio y API Key). 

Importando culqi-go:

```go
import (    
    "github.com/brayancruces/culqi-go"
    "github.com/brayancruces/culqi-go/{{recurso}}"
)
```

> **Nota:** Una vez importado  el `culqi-go`, también es necesario importar el paquete del recurso o los recursos que vamos a utilizar (token, charge, plan, suscription o refund). Reemplazar `{{recurso}}` por el nombre del recurso.

Realizando configuración del cliente
```go
func main() {

  // 1. Configuración
  config := &culqi.Config{
    MerchantCode:   "pk_test_xxx",  // Código de tu Comercio
    ApiKey:   "sk_test_xxx", // API Key
    //ApiVersion: "v2",   // No es un parametro necesario, por defecto es la v2
  }

  // 2. Crea un nuevo cliente
  client := culqi.New(config)
}
```
### Crear un *token* 


```go
  // 3. Parametros de creación de token
  params := &token.TokenParams{
    FirstName: "Brayan",
    LastName: "Cruces",
    Email: "brayancruces@gmail.com",
    Currency: "PEN",
    CardNumber: 4111111111111111,
    Cvv: 123,
    ExpMonth: 9,
    ExpYear: 2020,
  }

  // 4. Crear Token
  resp, err := token.Create(params, client)

  if err != nil {
      panic(err.Error())
  }

```

### Crear un *cargo* (charge)

```
Code

```

### Crear un *plan* 

```
Code

```


### Crear una *suscripción* (suscription)  

```
Code

```


### Devolver un cargo (refund)

```
Code

```


## Ejemplos 

- Creación de un cargo 
- Obtener listado de cargos 


## Tests 

```bash
$ tests
```

---

## Documentación 

¿Necesitas más información para integrar `culqi-go`? La documentación completa se encuentra en https://developers.culqi.com


## Licencia 

El código fuente de `culqi-go` está distribuido bajo MIT License, revisar el archivo [LICENSE](LICENSE).


## Contribuir

TO-DO


## Changelog

Todos los cambios en las versiones de esta biblioteca están listados en [CHANGELOG](CHANGELOG).   


## Autor

Brayan Cruces ([@theboss](https://github.com/brayancruces) - Team Culqi)  

## Todo 
- Añadir más ejemplos 
- Métodos (listar, get)
