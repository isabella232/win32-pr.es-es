---
title: Registro W3C
description: El registro extendido W3C es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor o en el grupo de direcciones URL.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b253daebae22a2b99e152451cff360c7b633ca64
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789772"
---
# <a name="w3c-logging"></a>Registro W3C

El registro extendido W3C es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor o en el grupo de direcciones URL. Cuando el registro W3C está habilitado en un grupo de direcciones URL, el registro solo se realiza en las solicitudes que se enrutan al grupo de direcciones URL. Se crea un archivo de registro independiente para cada grupo de direcciones URL configurado para habilitar el registro W3C.

Cuando el registro W3C está habilitado en la sesión de servidor, funciona como una forma centralizada de registro para todos los grupos de direcciones URL en la sesión de servidor. Se mantiene un único archivo de registro para todos los grupos de direcciones URL en la sesión de servidor.

En la tabla siguiente se enumeran los campos que puede registrar la API del servidor HTTP. La tabla contiene un subconjunto de las constantes de [**\_ \_ campo de registro http**](http-log-field--constants.md) . Algunos de los campos que se enumeran a continuación se generan automáticamente mediante la API de servidor HTTP internamente y, por lo tanto, no se incluyen en la estructura de [**\_ datos de \_ campos \_ de registro http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) . La columna "aparece como" contiene el texto que aparece en el archivo de registro. Los datos de la tabla están en el orden de aparición en el registro del archivo de registro.

Los campos que no están marcados como "API del servidor HTTP generado" deben pasarse dentro de la estructura de [**\_ datos de \_ campos \_ de registro http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) por aplicación. La aplicación podría generar esos campos a partir de la estructura de la [**\_ solicitud HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) que se le ha pasado.



| Campo                            | Aparece como      | Descripción                                                                                                                                | \_Miembro de \_ datos de campos de registro http \_ | Constantes de campos de \_ registro http \_      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Fecha                             | fecha            | Fecha en la que se produjo la actividad.                                                                                                   | API del servidor HTTP generada.     | \_fecha del \_ campo de registro http \_           |
| Hora                             | time            | La hora, en hora universal coordinada (UTC), a la que se produjo la actividad.                                                             | API del servidor HTTP generada.     | \_hora del \_ campo de registro http \_           |
| Nombre del servicio y número de instancia | s-siteName      | El nombre del servicio de Internet y el número de instancia que se estaba ejecutando en el cliente.                                                              | ServiceName                    | \_nombre del \_ sitio del campo de registro http \_ \_     |
| Nombre del servidor                      | s-COMPUTERNAME  | Nombre del servidor en el que se generó la entrada del archivo de registro.                                                                          | nombreDeServidor                     | \_nombre de \_ equipo del campo de registro http \_ \_ |
| Dirección IP del servidor                | s-IP            | Dirección IP del servidor en el que se generó la entrada del archivo de registro.                                                                    | ServerIp                       | \_IP de \_ servidor de campo de registro http \_ \_     |
| Método                           | CS-Method       | El verbo solicitado, por ejemplo, un método GET.                                                                                             | Método                         | \_método de \_ campo de registro http \_         |
| Recurso de URI                         | CS-URI-tallo     | El destino del verbo, por ejemplo, Default.htm.                                                                                          | UriStem                        | \_recurso de \_ URI de campo de registro http \_ \_      |
| Consulta de URI                        | CS-URI-Query    | La consulta, si la hay, que el cliente estaba intentando realizar. Las consultas de Identificador de recursos universal (URI) solo son necesarias para las páginas dinámicas. | UriQuery                       | \_consulta de \_ URI de campo de registro http \_ \_     |
| Puerto del servidor                      | s-Port          | Número de puerto del servidor que está configurado para el servicio.                                                                                 | ServerPort                     | \_Puerto de \_ servidor de campo de registro http \_ \_   |
| Nombre de usuario                        | CS-username     | Nombre del usuario autenticado que tuvo acceso al servidor. Los usuarios anónimos se indican con un guion.                                    | UserName                       | \_nombre de \_ usuario del campo de registro http \_ \_     |
| Dirección IP de cliente                | c-ip            | Dirección IP del cliente que realizó la solicitud.                                                                                        | ClientIp                       | \_ \_ \_ dirección IP del cliente del campo de registro http \_     |
| Versión de protocolo                 | versión CS      | La versión del protocolo HTTP que usó el cliente.                                                                                            | API del servidor HTTP generada.     | \_versión del \_ campo de registro http \_        |
| User Agent                       | CS (User-Agent)  | Tipo de explorador utilizado por el cliente.                                                                                                     | UserAgent                      | \_agente de \_ usuario de campo de registro http \_ \_    |
| Cookie                           | CS (cookie)      | El contenido de la cookie enviada o recibida, si existe.                                                                                        | Cookie                         | \_cookie de \_ campo de registro http \_         |
| Referrer                         | CS (referrer)    | El sitio que el usuario visitó por última vez. Este sitio proporciona un vínculo al sitio actual.                                                        | Referrer                       | \_referencia de \_ campo de registro http \_       |
| Host                             | CS-host         | Nombre del encabezado de host, si existe.                                                                                                              | Host                           | \_host de \_ campo de registro http \_           |
| Estado HTTP                      | SC-estado       | El código de estado HTTP.                                                                                                                      | ProtocolStatus                 | \_Estado del \_ campo de registro http \_         |
| Subestado del Protocolo               | SC-subestado    | Código de error de subestado.                                                                                                                  | SubStatus                      | \_subestado de campo de registro http \_ \_ \_    |
| Estado de Win32                     | SC-Win32-estado | Código de estado de Windows.                                                                                                                   | Win32Status                    | \_Campo de registro http \_ \_ Estado de Win32 \_  |
| Bytes enviados                       | SC-bytes        | Número de bytes enviados por el servidor.                                                                                                    | API del servidor HTTP generada.     | \_bytes de campos de registro http \_ \_ \_ enviados    |
| Bytes recibidos                   | CS-bytes        | El número de bytes recibidos y procesados por el servidor.                                                                                  | API del servidor HTTP generada.     | \_bytes de campo de registro http \_ \_ \_ recibidos    |
| Tiempo empleado                       | tiempo de espera      | El período de tiempo que tardó la acción, en milisegundos.                                                                                  | API del servidor HTTP generada.     | tiempo de los \_ campos de registro http \_ \_ \_ tomados    |
| IDENTIFICADOR de flujo                      | streamid          | El identificador de la secuencia.                                                                                  | API del servidor HTTP generada.     | \_identificador de \_ flujo de campo de registro http \_ \_       |



 

El archivo de registro es un formato basado en texto ASCII personalizable. Los prefijos de campo del archivo se definen de la siguiente manera:

|     |                           |
|-----|---------------------------|
| s   | Acciones del servidor.           |
| c   | Acciones de cliente.           |
| seguro  | Acciones de servidor a cliente. |
| cs  | Acciones de cliente a servidor. |



 

La aplicación puede seleccionar uno o varios de los campos del archivo de registro extendido W3C; sin embargo, no todos los campos contendrán información. En el caso de los campos seleccionados pero para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza con un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y saltos de línea que, si no se reemplazan por el signo más (+), interrumpiría el formato del archivo de registro. Los campos están separados por espacios.

Si un campo está habilitado por el grupo de direcciones URL o la sesión del servidor, pero no se ha seleccionado para la solicitud, aparece en el archivo de registro con un guión (-) como marcador de posición.

Los archivos de registro se crean cuando la primera solicitud llega al grupo de direcciones URL o a la sesión del servidor, no se crean al configurar el registro. En el ejemplo siguiente se muestra la primera entrada de archivo de registro de un archivo de registro de W3C con los campos de dirección IP de cliente, nombre de usuario, dirección IP del servidor, Puerto del servidor, método, recurso visitado del URI, consulta de URI, estado y agente de usuario habilitado:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

El campo de tiempo invertido se inicializa cuando la API del servidor HTTP recibe el primer byte, antes de que se analice la solicitud. La marca de tiempo que se tarda en realizarse se detiene cuando se realiza la última operación de envío. El tiempo invertido no refleja el tiempo a lo largo de la red. La primera solicitud al sitio muestra un tiempo ligeramente mayor que otras solicitudes similares, ya que la API del servidor HTTP abre el archivo de registro con la primera solicitud.

 

 