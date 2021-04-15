---
title: Valores de configuración
description: El comportamiento de la API del punto de control y la API del host del dispositivo se puede modificar cambiando la configuración del registro.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695256"
---
# <a name="configuration-settings"></a>Valores de configuración

El comportamiento de la [API del punto de control](control-point-api.md) y la [API del host del dispositivo](device-host-api.md) se puede modificar cambiando la configuración del registro.

Hay siete valores del registro que afectan al comportamiento:

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\Host de dispositivo **UPnP** \\ **Límite de tamaño de archivo**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Límite de tamaño de archivo**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

Hay dos valores de registro denominados **límite de tamaño de archivo**, uno para los documentos de Descripción y el otro para las respuestas que utilizan el Protocolo simple de acceso a objetos (SOAP).

La ubicación de cada uno de los siete valores del registro es la siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a>Descripciones de valores del registro

Los valores del registro se explican en la lista siguiente. Cada valor del registro es **una \_ DWORD** de tipo REG (un entero de 32 bits). El efecto de cada valor es global.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

Especifica las direcciones IP válidas para la dirección URL del documento de Descripción del dispositivo. Si la dirección IP del host que se especifica en la dirección URL del documento de descripción no está dentro del ámbito especificado por **DownloadScope**, esa dirección IP no es válida y el objeto de dispositivo no se creará.

En la tabla siguiente se muestran los valores válidos. El valor predeterminado es 1.



| Valor de **DownloadScope** | Significado                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | La dirección IP del host debe ser una dirección de subred.                                                                                                                                                                |
| 1                          | La dirección IP del host debe ser una dirección de subred o una dirección privada que sea de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (según se especifica en RFC 1918) o 169,254. *x*. *x* (según se especifica en RFC 3330). |
| 2                          | La dirección IP del host debe ser una dirección de subred, una dirección privada o una dirección que se encuentre dentro de los saltos del período de vida (TTL) desde el punto de control.                                                              |
| 3                          | La dirección IP del host puede ser cualquier dirección.                                                                                                                                                                      |
| >3                      | Igual que para el valor 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

Opcional. Especifica la duración de un dispositivo, en segundos, que invalida el valor proporcionado en el mensaje del anuncio del dispositivo. Si **DeviceLifeTime** está presente, se omite el valor especificado en el anuncio del dispositivo y, en su lugar, se usa el valor del registro. Esto se aplica a todos los dispositivos.

Los valores válidos van de 900 a **\_ DWORD máx**. El valor predeterminado es 1800. Si **DeviceLifeTime** se establece en 0, se usa el valor predeterminado.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Host de dispositivo **UPnP** \\ **Límite de tamaño de archivo**
</dt> <dd>

Especifica el tamaño máximo, en bytes, de cada documento de descripción. Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2. En las versiones anteriores, esta configuración se codifica de forma rígida como 102400.

Los valores válidos van de 10240 a **\_ DWORD máx**. El valor predeterminado es 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Límite de tamaño de archivo**
</dt> <dd>

Especifica el tamaño máximo, en bytes, de la respuesta SOAP que es aceptable. Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2. En las versiones anteriores, esta configuración se codifica de forma rígida como 102400.

Los valores válidos van de 10240 a **\_ DWORD máx**. El valor predeterminado es 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

Especifica el número máximo de entradas permitidas en la memoria caché del Protocolo simple de detección de servicios (SSDP).

Los valores válidos oscilan entre 10 y 30000. El valor predeterminado es 1000.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**PERÍODO**
</dt> <dd>

Especifica el período de vida de un paquete SSDP. Es decir, **TTL** especifica el número de saltos permitido para un paquete.

Los valores válidos oscilan entre 1 y 255. El valor predeterminado es 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

Especifica las direcciones IP que son orígenes válidos de un mensaje. Si un mensaje entrante se origina en una dirección que no está dentro del ámbito especificado por **ReceiveScope**, se omite el mensaje. Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2. En las versiones anteriores, se acepta un mensaje sin tener en cuenta su origen.

En la tabla siguiente se muestran los valores válidos. El valor predeterminado es 1.



| Valor de **ReceiveScope** | Significado                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | La dirección IP del remitente debe ser una dirección de subred.                                                                                                                                                                |
| 1                         | La dirección IP del remitente debe ser una dirección de subred o una dirección privada que sea de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (según se especifica en RFC 1918) o 169,254. *x*. *x* (según se especifica en RFC 3330). |
| 2                         | No se utiliza. Si **ReceiveScope** se establece en 2, se utiliza el valor predeterminado.                                                                                                                                        |
| 3                         | La dirección IP del remitente puede ser cualquier dirección.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la arquitectura de UPnP](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




