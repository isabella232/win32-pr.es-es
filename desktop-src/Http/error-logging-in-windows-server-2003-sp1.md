---
title: Error al iniciar sesión Windows Server 2003 SP1
description: Error al iniciar sesión Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Error al iniciar sesión Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014813"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Error al iniciar sesión Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Adición de encabezados de estilo W3C

A partir de Windows Server 2003 con Service Pack 1 (SP1), el registro de errores de la API del servidor HTTP incluye encabezados de estilo W3C que permiten analizar archivos de registro mediante analizadores de registro estándar. La plantilla que se muestra a continuación muestra todos los campos que se pueden registrar en el archivo de registro de errores HTTP.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Registro de campos adicionales

El registro de errores HTTP se ha ampliado para incluir nueve campos más para registrar datos sobre los errores que se producen. Los nuevos campos de error se enumeran a continuación:

-   Nombre del equipo servidor \[ S-COMPUTERNAME\]
-   Agente de \[ usuario CS(AGENTE \_ DE USUARIO)\]
-   Cookie \[ CS(COOKIE)\]
-   referrer \[ CS(referrer)\]
-   Nombre de \[ host CS-HOST\]
-   Bytes recibidos por el \[ servidor SC-BYTES\]
-   Bytes recibidos y procesados por el \[ servidor CS-BYTES\]
-   Tiempo que se necesita para procesar la \[ solicitud TIME-TAKEN\]
-   Queue-Name (reservado para IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selección de fileds para registrar en el archivo de registro de errores HTTP

Se ha agregado la clave del Registro **ErrorLoggingFields** para controlar los campos registrados en el registro de errores HTTP. Estos valores del Registro se encuentran en una clave de parámetros HTTP \\ ubicada en:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

El **valor del Registro ErrorLoggingFields** es un valor DWORD que contiene valores de bits para cada uno de los campos que se pueden registrar. Para habilitar el registro de un campo específico, establezca su valor de bit correspondiente en 1 y reinicie el servicio HTTP. Para deshabilitar el registro, establezca el valor de bit en 0. Para configurar varios campos, use un OR bit a bit de los valores individuales. Por ejemplo, para activar los campos de registro Cookie y Referrer, el valor debe ser 0x00020000 \| 0x00040000 = 0x00060000. Si la **clave del Registro ErrorLoggingFields** no está presente, se registran los campos predeterminados. El **valor ErrorLoggingFields** para registrar los campos predeterminados es 0x7c884c7. Para habilitar el registro de todos los campos que se muestran en la tabla siguiente, establezca el valor en 0x7dff4e7.

Los campos de registro de errores se enumeran en la tabla siguiente:



| Campo de registro            | Registrado de forma predeterminada | Valor de bit  |
|----------------------|-------------------|------------|
| Date                 | Sí               | 0x00000001 |
| Time                 | Sí               | 0x00000002 |
| Nombre del equipo del servidor | No                | 0x00000020 |
| Dirección IP de cliente    | Sí               | 0x00000004 |
| Puerto de cliente          | Sí               | 0x00400000 |
| Dirección IP del servidor    | Sí               | 0x00000040 |
| Puerto del servidor          | Sí               | 0x00008000 |
| Versión del protocolo     | Sí               | 0x00080000 |
| Método               | Sí               | 0x00000080 |
| URI                  | Sí               | 0x00800000 |
| User Agent           | No                | 0x00010000 |
| Cookie               | No                | 0x00020000 |
| Referente             | No                | 0x00040000 |
| Host                 | No                | 0x00100000 |
| Estado del protocolo      | Sí               | 0x00000400 |
| SC-Bytes             | No                | 0x00001000 |
| CS-Bytes             | No                | 0x00002000 |
| Tiempo empleado           | No                | 0x00004000 |
| SiteId               | Sí               | 0x01000000 |
| Frase de motivo        | Sí               | 0x02000000 |
| Nombre de la cola           | No                | 0x04000000 |
| Id. de flujo            | No                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Suversión de fecha y hora

De forma predeterminada, se crea un nuevo archivo de registro de errores HTTP (lo que se denomina suversión de archivos) cuando el archivo de registro actual alcanza un tamaño especificado. A partir de Windows Server 2003 con SP1, se pueden crear nuevos archivos de registro de errores en función de la fecha y hora. La suversión de fecha y hora se controla mediante dos nuevos valores del Registro: **ErrorLoggingRolloverType** y **ErrorLoggingLocaltimeRollover**. Para habilitar la suversión de fecha y hora, estos valores del Registro deben agregarse al registro. El servicio Http debe reiniciarse cuando estas claves se agregan al Registro. Las claves del Registro de suversión del archivo de registro se crean con la siguiente clave:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

La **clave del Registro ErrorLoggingRolloverType** indica el tipo de suversión deseada y se establece de forma predeterminada en la suversión basada en el tamaño. La suversión también se puede establecer para que se produzca diariamente, semanal, mensual o por hora. Cuando la suversión de archivos se basa en el tiempo, un valor **de ErrorLoggingLocaltimeRollover** de 0 indica que la hora de su desplazamiento se expresa en GMT y un valor de 1 indica que la hora de su desplazamiento se expresa en la hora local. La **clave ErrorLoggingRolloverType** puede tomar un valor de 0 a 4 como se muestra en la tabla siguiente.



| Valor de tipo de suversión | Descripción                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Suversión basada en el tamaño. Los archivos de registro se revierte cuando el archivo alcanza el tamaño definido en la clave del Registro **ErrorLogFileTruncateSize.** |
| 1                   | La suversión del archivo de registro se produce a diario.                                                                                                         |
| 2                   | La suversión del archivo de registro se produce semanalmente.                                                                                                        |
| 3                   | La suversión del archivo de registro se produce mensualmente.                                                                                                       |
| 4                   | La suversión del archivo de registro se produce cada hora.                                                                                                        |



 

Las convenciones de nomenclatura para los archivos que almacenan los registros de errores son diferentes para la suversión basada en el tamaño, la fecha y la hora. En la tabla siguiente se enumeran las convenciones de nomenclatura para los archivos de registro HTTP.



| Tipo tollover | Nombre del archivo de registro  | Descripción                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Size          | HTTPERRn.LOG   | El archivo de registro se recicla cuando alcanza un tamaño específico. n es el número de archivo y se incrementa cuando se revierte el archivo de registro. |
| Diario         | htYYMMDD.log   | El archivo de registro se recicla diariamente.                                                                                                     |
| Semanalmente        | htYYMMww.log   | El archivo de registro se recicla semanalmente, donde ww es la semana del mes.                                                                 |
| Mensualmente       | htYYMM.log     | El archivo de registro se recicla cada mes.                                                                                               |
| Cada hora        | htYYMMDDhh.log | El archivo de registro se recicla cada hora, donde hh es la hora del día expresada en una notación de 0 a 24 horas.                                   |



 

 

 




