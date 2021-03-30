---
title: Registro de errores en Windows Server 2003 SP1
description: Registro de errores en Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Registro de errores en Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/14/2019
ms.locfileid: "103784876"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Registro de errores en Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Adición de encabezados de estilo W3C

A partir de Windows Server 2003 con Service Pack 1 (SP1), el registro de errores de la API del servidor HTTP incluye encabezados de estilo W3C que permiten analizar los archivos de registro mediante analizadores de registro estándar. En la plantilla que se muestra a continuación se enumeran todos los campos que se pueden registrar en el archivo de registro de errores http.

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

El registro de errores HTTP se ha ampliado para incluir nueve campos más para registrar los datos de los errores que se producen. Los campos de error nuevos se enumeran a continuación:

-   Nombre de equipo \[ del servidor S-COMPUTERNAME\]
-   User Agent \[ CS (agente de usuario \_ )\]
-   Cookie \[ CS (cookie)\]
-   referencia \[ CS (referrer)\]
-   Nombre \[ de host CS-host\]
-   Bytes recibidos por el servidor \[ SC-bytes\]
-   Bytes recibidos y procesados por el servidor \[ CS-bytes\]
-   Tiempo necesario para procesar el \[ tiempo de solicitud\]
-   Queue-Name (reservado para IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selección de los archivos que se van a registrar en el archivo de registro de errores HTTP

La clave del registro **ErrorLoggingFields** se ha agregado para controlar los campos que se registran en el registro de errores http. Estos valores del registro se encuentran en una \\ clave http Parameters, que se encuentra en:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

El valor del registro **ErrorLoggingFields** es un valor DWORD que contiene valores de bits para cada uno de los campos que se pueden registrar. Para habilitar el registro de un campo específico, establezca el valor de bit correspondiente en 1 y reinicie el servicio HTTP. Para deshabilitar el registro, establezca el valor de bit en 0. Para configurar varios campos, use una operación OR bit a bit de los valores individuales. Por ejemplo, para activar los campos cookie y registro de referencia, el valor debe ser 0x00020000 \| 0x00040000 = 0x00060000. Si la clave del registro **ErrorLoggingFields** está ausente, se registran los campos predeterminados. El valor de **ErrorLoggingFields** para registrar los campos predeterminados es 0x7c884c7. Para habilitar el registro de todos los campos que se muestran en la tabla siguiente, establezca el valor en 0x7dff4e7.

Los campos de registro de errores se muestran en la tabla siguiente:



| Campo de registro            | Registrado de forma predeterminada | Valor de bit  |
|----------------------|-------------------|------------|
| Date                 | Sí               | 0x00000001 |
| Hora                 | Sí               | 0x00000002 |
| Nombre del equipo servidor | No                | 0x00000020 |
| Dirección IP de cliente    | Sí               | 0x00000004 |
| Puerto de cliente          | Sí               | 0x00400000 |
| Dirección IP del servidor    | Sí               | 0x00000040 |
| Puerto del servidor          | Sí               | 0x00008000 |
| Versión de protocolo     | Sí               | 0x00080000 |
| Método               | Sí               | 0x00000080 |
| URI                  | Sí               | 0x00800000 |
| User Agent           | No                | 0x00010000 |
| Cookie               | No                | 0x00020000 |
| referencia             | No                | 0x00040000 |
| Host                 | No                | 0x00100000 |
| Estado del Protocolo      | Sí               | 0x00000400 |
| SC-Bytes             | No                | 0x00001000 |
| CS-Bytes             | No                | 0x00002000 |
| Tiempo empleado           | No                | 0x00004000 |
| Cuyo               | Sí               | 0x01000000 |
| Frase del motivo        | Sí               | 0x02000000 |
| Nombre de la cola           | No                | 0x04000000 |
| Identificador de flujo            | No                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Sustitución de fecha y hora

De forma predeterminada, se crea un nuevo archivo de registro de errores HTTP (sustitución de archivos con términos) cuando el archivo de registro actual alcanza un tamaño especificado. A partir de Windows Server 2003 con SP1, se pueden crear nuevos archivos de registro de errores en función de la fecha y la hora. La sustitución de fecha y hora se controla mediante dos nuevos valores del registro: **ErrorLoggingRolloverType** y **ErrorLoggingLocaltimeRollover**. Para habilitar la sustitución de fecha y hora, estos valores del registro se deben agregar al registro. El servicio http debe reiniciarse cuando estas claves se agreguen al registro. Las claves del registro de sustitución del archivo de registro se crean con la siguiente clave:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

La clave del registro **ErrorLoggingRolloverType** indica el tipo de sustitución deseada y se establece de forma predeterminada en sustitución basada en el tamaño. La sustitución también puede configurarse para que se produzca diariamente, semanalmente, mensualmente o cada hora. Cuando la sustitución de archivos se basa en el tiempo, un valor de **ErrorLoggingLocaltimeRollover** de 0 indica que la hora de sustitución se expresa en GMT y un valor de 1 indica que la hora de sustitución se expresa en hora local. La clave **ErrorLoggingRolloverType** puede tomar un valor de 0 a 4, como se muestra en la tabla siguiente.



| Valor de tipo de sustitución incremental | Descripción                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Sustitución basada en el tamaño. Los archivos de registro se revierten cuando el archivo alcanza el tamaño definido en la clave del registro **ErrorLogFileTruncateSize** . |
| 1                   | La sustitución del archivo de registro se produce diariamente.                                                                                                         |
| 2                   | La sustitución del archivo de registro se produce semanalmente.                                                                                                        |
| 3                   | La sustitución del archivo de registro se produce mensualmente.                                                                                                       |
| 4                   | La sustitución del archivo de registro se produce cada hora.                                                                                                        |



 

Las convenciones de nomenclatura para los archivos que almacenan los registros de errores son diferentes para el tamaño, la fecha y la sustitución basada en el tiempo. En la tabla siguiente se enumeran las convenciones de nomenclatura para los archivos de registro http.



| Tipo Tollover | Nombre del archivo de registro  | Descripción                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Size          | HTTPERRn. LOG   | El archivo de registro se recicla cuando alcanza un tamaño específico. n es el número de archivo y se incrementa cuando el archivo de registro se revierte. |
| Diario         | htYYMMDD. log   | El archivo de registro se recicla diariamente.                                                                                                     |
| Cada semana        | htYYMMww. log   | El archivo de registro se recicla semanalmente, donde WW es la semana del mes.                                                                 |
| Mensual       | htYYMM. log     | El archivo de registro se recicla cada mes.                                                                                               |
| Cada hora        | htYYMMDDhh. log | El archivo de registro se recicla cada hora, donde HH es la hora del día expresada en notación de 0-24 hora.                                   |



 

 

 




