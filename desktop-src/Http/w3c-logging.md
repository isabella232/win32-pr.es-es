---
title: Registro de W3C
description: El registro extendido de W3C es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor o en el grupo de direcciones URL.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa67d2e0141dfb936ea44070479560ca90e9c3720db8ffebedf5af20b0442dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078305"
---
# <a name="w3c-logging"></a>Registro de W3C

El registro extendido de W3C es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor o en el grupo de direcciones URL. Cuando el registro de W3C está habilitado en un grupo de direcciones URL, el registro solo se realiza en las solicitudes que se enruta al grupo de direcciones URL. Se crea un archivo de registro independiente para cada grupo de direcciones URL configurado para habilitar el registro de W3C.

Cuando el registro de W3C está habilitado en la sesión del servidor, funciona como forma centralizada de registro para todos los grupos de direcciones URL de la sesión del servidor. Se mantiene un único archivo de registro para todos los grupos de direcciones URL de la sesión del servidor.

En la tabla siguiente se enumeran los campos que puede registrar la API del servidor HTTP. La tabla contiene un subconjunto de las [**constantes \_ HTTP LOG \_ FIELD.**](http-log-field--constants.md) Algunos de los campos que se enumeran a continuación son generados automáticamente por la API del servidor HTTP internamente y, por tanto, no se incluyen en la estructura DE DATOS [**DE CAMPOS \_ DE \_ \_ REGISTRO HTTP.**](/windows/desktop/api/Http/ns-http-http_log_fields_data) La columna "Aparece como" contiene el texto que aparece en el archivo de registro. Los datos de la tabla están en el orden de aparición en el registro del archivo de registro.

Los campos que no están marcados como "HTTP Server API generated" deben pasarse dentro de la estructura DE DATOS [**DE CAMPOS \_ \_ \_ DE**](/windows/desktop/api/Http/ns-http-http_log_fields_data) REGISTRO HTTP por aplicación. La aplicación podría generar esos campos a partir de la [**estructura \_ HTTP REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) que se le ha pasado.



| Campo                            | Aparece como      | Descripción                                                                                                                                | Miembro \_ DE DATOS DE CAMPOS DE REGISTRO \_ \_ HTTP | Constantes \_ DE CAMPOS DE REGISTRO \_ HTTP      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Fecha                             | fecha            | Fecha en la que se produjo la actividad.                                                                                                   | API de servidor HTTP generada.     | FECHA \_ DEL CAMPO DE REGISTRO \_ \_ HTTP           |
| Time                             | time            | Hora, en hora universal coordinada (UTC), a la que se produjo la actividad.                                                             | API de servidor HTTP generada.     | HORA DEL \_ CAMPO \_ DE REGISTRO \_ HTTP           |
| Nombre de servicio y número de instancia | s-sitename      | El nombre del servicio de Internet y el número de instancia que se ejecutaba en el cliente.                                                              | ServiceName                    | NOMBRE \_ DE SITIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP     |
| Nombre del servidor                      | s-computername  | Nombre del servidor en el que se generó la entrada del archivo de registro.                                                                          | nombreDeServidor                     | NOMBRE \_ DE EQUIPO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP |
| Dirección IP del servidor                | s-ip            | Dirección IP del servidor en el que se generó la entrada del archivo de registro.                                                                    | ServerIp                       | DIRECCIÓN IP \_ DEL SERVIDOR DEL CAMPO DE REGISTRO \_ \_ \_ HTTP     |
| Método                           | cs-method       | Verbo solicitado, por ejemplo, un método GET.                                                                                             | Método                         | MÉTODO \_ DE CAMPO DE REGISTRO \_ \_ HTTP         |
| Lemat de URI                         | cs-uri-stem     | Destino del verbo, por ejemplo, Default.htm.                                                                                          | UriStem                        | HTTP \_ LOG \_ FIELD \_ URI \_ STEM      |
| Consulta DE URI                        | cs-uri-query    | Consulta, si la hay, que el cliente estaba intentando realizar. Las consultas de Identificador de recursos universal (URI) solo son necesarias para las páginas dinámicas. | UriQuery                       | CONSULTA DE URI \_ DE CAMPO DE REGISTRO \_ \_ \_ HTTP     |
| Puerto del servidor                      | s-port          | Número de puerto del servidor que está configurado para el servicio.                                                                                 | ServerPort                     | PUERTO \_ DEL SERVIDOR DEL CAMPO DE REGISTRO \_ \_ \_ HTTP   |
| Nombre de usuario                        | cs-username     | Nombre del usuario autenticado que ha accedido al servidor. Los usuarios anónimos se indican con un guion.                                    | UserName                       | NOMBRE \_ DE USUARIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP     |
| Dirección IP de cliente                | c-ip            | Dirección IP del cliente que realizó la solicitud.                                                                                        | ClientIp                       | DIRECCIÓN IP \_ DE CLIENTE DEL CAMPO DE REGISTRO \_ \_ \_ HTTP     |
| Versión del protocolo                 | cs-version      | Versión del protocolo HTTP que usó el cliente.                                                                                            | API de servidor HTTP generada.     | VERSIÓN \_ DEL CAMPO DE REGISTRO \_ \_ HTTP        |
| User Agent                       | cs(User-Agent)  | Tipo de explorador utilizado por el cliente.                                                                                                     | UserAgent                      | AGENTE \_ DE USUARIO DEL CAMPO DE REGISTRO \_ \_ \_ HTTP    |
| Cookie                           | cs(Cookie)      | Contenido de la cookie enviada o recibida, si la hay.                                                                                        | Cookie                         | COOKIE \_ DE CAMPO DE REGISTRO \_ \_ HTTP         |
| Referrer                         | cs(Referrer)    | El sitio que visitó por última vez el usuario. Este sitio proporciona un vínculo al sitio actual.                                                        | Referrer                       | HTTP \_ LOG \_ FIELD \_ REFERRER       |
| Host                             | cs-host         | Nombre del encabezado de host, si lo hay.                                                                                                              | Host                           | HOST \_ DE CAMPO DE REGISTRO \_ \_ HTTP           |
| Estado HTTP                      | sc-status       | El código de estado HTTP.                                                                                                                      | ProtocolStatus                 | ESTADO DEL \_ CAMPO \_ DE REGISTRO \_ HTTP         |
| Subestado del protocolo               | sc-substatus    | Código de error de subestado.                                                                                                                  | SubStatus                      | \_ \_ SUBESESTACIÓN DE CAMPO \_ DE REGISTRO \_ HTTP    |
| Estado de Win32                     | sc-win32-status | El Windows de estado.                                                                                                                   | Win32Status                    | ESTADO DE \_ \_ WIN32 DEL CAMPO \_ DE REGISTRO \_ HTTP  |
| Bytes enviados                       | sc-bytes        | Número de bytes enviados por el servidor.                                                                                                    | API de servidor HTTP generada.     | BYTES \_ DE CAMPO DE REGISTRO HTTP \_ \_ \_ ENVIADOS    |
| Bytes recibidos                   | cs-bytes        | Número de bytes recibidos y procesados por el servidor.                                                                                  | API de servidor HTTP generada.     | HTTP \_ LOG \_ FIELD \_ BYTES \_ RECV    |
| Tiempo empleado                       | tiempo de espera      | El período de tiempo que tardó la acción, en milisegundos.                                                                                  | API de servidor HTTP generada.     | TIEMPO \_ DE CAMPO DE REGISTRO HTTP \_ \_ \_ REALIZADO    |
| Id. de flujo                      | streamid          | Id. de flujo.                                                                                  | API de servidor HTTP generada.     | IDENTIFICADOR DE \_ FLUJO DE CAMPO DE REGISTRO \_ \_ \_ HTTP       |



 

El archivo de registro es un formato basado en texto ASCII personalizable. Los prefijos de campo del archivo se definen de la siguiente manera:

| Prefijo    | Descripción                          |
|-----|---------------------------|
| s   | Acciones del servidor.           |
| c   | Acciones de cliente.           |
| Sc  | Acciones de servidor a cliente. |
| cs  | Acciones de cliente a servidor. |



 

La aplicación puede seleccionar uno o varios de los campos del archivo de registro extendido de W3C, pero no todos los campos contendrán información. Para los campos seleccionados pero para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza por un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y avances de línea que, si no se reemplazan por el signo más (+), interrumpirían el formato del archivo de registro. Los campos están separados por espacios.

Si un campo está habilitado por el grupo de direcciones URL o la sesión del servidor, pero no está seleccionado para la solicitud, aparece en el archivo de registro con un guion (-) como marcador de posición.

Los archivos de registro se crean cuando la primera solicitud llega a la sesión de servidor o grupo de direcciones URL, no se crean cuando se configura el registro. En el ejemplo siguiente se muestra la primera entrada de archivo de registro para un archivo de registro W3C con los campos Ip de cliente, Nombre de usuario, DIRECCIÓN IP del servidor, Puerto del servidor, Método, Lemat uri, Consulta de URI, Estado y Agente de usuario habilitados:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

El campo time-taken se inicializa cuando la API del servidor HTTP recibe el primer byte, antes de analizar la solicitud. La marca de tiempo de tiempo que se toma se detiene cuando se produce la última finalización de envío. El tiempo necesario no refleja el tiempo a través de la red. La primera solicitud al sitio muestra un tiempo ligeramente más largo que otras solicitudes similares porque la API del servidor HTTP abre el archivo de registro con la primera solicitud.

 

 