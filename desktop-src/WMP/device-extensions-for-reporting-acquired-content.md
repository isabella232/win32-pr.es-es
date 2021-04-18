---
title: Extensiones de dispositivo para la generación de informes de contenido adquirido
description: Extensiones de dispositivo para la generación de informes de contenido adquirido
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Windows Media Player, informes de contenido adquirido
- extensiones de dispositivos, informes de contenido adquirido
- extensiones, informes de contenido adquirido
- informes de contenido adquirido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831312457427cc9fe4ceed004772f3b174f77989
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695400"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Extensiones de dispositivo para la generación de informes de contenido adquirido

Windows Media Player 11 presenta una nueva funcionalidad que permite a los dispositivos portátiles notificar al reproductor el contenido que se agrega al dispositivo desde la última sincronización. Windows Media Player 11 puede usar esta información para copiar el contenido recién adquirido del dispositivo en el equipo del usuario. Los fabricantes de dispositivos deben tener en cuenta los siguientes requisitos para admitir esta funcionalidad:

-   Esta característica solo se admite para dispositivos habilitados para MTP.
-   Esta característica solo funciona con dispositivos que tienen una asociación con Windows Media Player.
-   Los dispositivos deben notificar solo el contenido que el dispositivo ha creado o descargado. Esto incluye las fotos tomadas por el dispositivo. grabaciones de voz creadas por el dispositivo; grabaciones de correo de voz; descarga desde una tarjeta de almacenamiento. y descargas de Internet. No se debe informar sobre el contenido que se almacenó en el dispositivo como resultado de la sincronización con otro dispositivo o de una asociación diferente.

El archivo de encabezado denominado wmpdevices. h, que se instala como parte del SDK de Windows Media Player, define las estructuras y constantes necesarias para admitir las extensiones de dispositivo de Windows Media Player.

Para que un dispositivo se reconozca como compatible con los informes de contenido adquirido a través del conjunto de extensiones de dispositivo MTP de Windows Media Player, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo de conjunto de los          | Orden de los campos | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11,0" |



 

En la tabla siguiente se proporcionan detalles acerca de la operación MTP para la generación de informes de contenido adquirido.



| Elemento                  | Descripción                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9202                                                                                                                                                                                                                          |
| Parámetro de operación 1 | El ID. de transacción proporcionado por el dispositivo durante la sesión anterior. Este valor es cero para la primera sesión.                                                                                                                |
| Parámetro de operación 2 | Índice de inicio. Este valor siempre es cero en la primera llamada de una sesión. En las llamadas posteriores dentro de la misma sesión de sincronización, este valor aumenta por el recuento de los elementos devueltos de los datos de respuesta anteriores. |
| Parámetro de operación 3 | 0x10000. Esta constante, definida en wmpdevices. h, es el número máximo de PUOIDs que se puede devolver en la respuesta. Tenga en cuenta que el valor de esta constante se puede revisar en futuras versiones de este archivo de encabezado.              |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                               |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                               |
| Datos                  | El dispositivo devuelve una matriz MTP que contiene PUOIDs que se han adquirido. La matriz comienza con un valor **DWORD** que indica el recuento de elementos de la matriz, seguido de la matriz de elementos.                               |
| Dirección de datos        | R->I                                                                                                                                                                                                                         |
| Opciones de código de respuesta | **MTP \_ RESPUESTA \_ correcta** (0x2001) o código de respuesta de error válido.                                                                                                                                                                    |
| Parámetro de respuesta 1  | IDENTIFICADOR de la transacción actual.                                                                                                                                                                                                     |
| Parámetro de respuesta 2  | El número de PUOIDs que quedan para ser recuperadas por solicitudes futuras.                                                                                                                                                            |
| Parámetro de respuesta 3  | **DWORD** que contiene información de estado. El estado se indica de forma bit a bit. Vea la sección Comentarios para obtener información sobre las marcas que se deben usar.                                                                                              |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                               |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

El estado se indica a través del parámetro de respuesta 3 de manera bit a bit mediante el siguiente marcador.



| Marca                                              | Value | Descripción                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ marca \_ \_ elementos adquiridos no notificados \_** | 0x1   | El dispositivo contiene algunos elementos adquiridos que no se pueden devolver en la lista de PUOIDS. Tenga en cuenta que esta marca no es redundante con el parámetro de respuesta 2. Establezca esta marca solo cuando haya elementos solicitados que el dispositivo no pueda devolver. |



 

Los bits 1 a 31 se reservan para uso futuro. Estos bits deben establecerse en cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




