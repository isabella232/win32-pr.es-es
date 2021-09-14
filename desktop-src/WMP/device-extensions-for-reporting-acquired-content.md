---
title: Extensiones de dispositivo para notificar contenido adquirido
description: Extensiones de dispositivo para notificar contenido adquirido
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Reproductor de Windows Media,extensiones de dispositivo
- Reproductor de Windows Media,extensions
- Reproductor de Windows Media, informes de contenido adquirido
- extensiones de dispositivo, informes de contenido adquirido
- extensiones, informes de contenido adquirido
- informes de contenido adquirido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831312457427cc9fe4ceed004772f3b174f77989
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068467"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Extensiones de dispositivo para notificar contenido adquirido

Reproductor de Windows Media 11 presenta una nueva funcionalidad que permite a los dispositivos portátiles notificar al reproductor el contenido agregado al dispositivo desde la última sincronización. Reproductor de Windows Media 11 puede usar esta información para copiar el contenido recién adquirido del dispositivo al equipo del usuario. Los fabricantes de dispositivos deben tener en cuenta los siguientes requisitos para admitir esta funcionalidad:

-   Esta característica solo se admite para dispositivos habilitados para MTP.
-   Esta característica solo funciona con dispositivos que tienen una asociación con Reproductor de Windows Media.
-   Los dispositivos solo deben notificar el contenido que el dispositivo ha escrito o descargado. Esto incluye las fotos tomadas por el dispositivo; grabaciones de voz creadas por el dispositivo; grabaciones de sonido; descargas de una tarjeta de almacenamiento; y descarga desde Internet. No se debe proporcionar información sobre el contenido almacenado en el dispositivo como resultado de la sincronización con otro dispositivo o una asociación diferente.

El archivo de encabezado denominado wmpdevices.h, que se instala como parte del SDK de Reproductor de Windows Media, define las estructuras y constantes necesarias para admitir Reproductor de Windows Media extensiones de dispositivo.

Para que un dispositivo se reconozca como compatible con los informes de contenido adquirido a través del conjunto de extensiones de dispositivo MTP de Reproductor de Windows Media, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo de conjunto de datos          | Orden de los campos | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11.0" |



 

En la tabla siguiente se proporcionan detalles sobre la operación MTP para notificar el contenido adquirido.



| Elemento                  | Descripción                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9202                                                                                                                                                                                                                          |
| Parámetro de operación 1 | Identificador de transacción proporcionado por el dispositivo durante la sesión anterior. Este valor es cero para la primera sesión.                                                                                                                |
| Parámetro de operación 2 | Índice inicial. Este valor siempre es cero en la primera llamada de una sesión. En las llamadas posteriores dentro de la misma sesión de sincronización, este valor aumenta por el recuento de los elementos devueltos de los datos de respuesta anteriores. |
| Parámetro de operación 3 | 0x10000. Esta constante, definida en wmpdevices.h, es el número máximo de PUOID que se pueden devolver en la respuesta. Tenga en cuenta que el valor de esta constante se puede revisar en futuras versiones de este archivo de encabezado.              |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                               |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                               |
| data                  | El dispositivo devuelve una matriz MTP que contiene puoids que se han adquirido. La matriz comienza con un **valor DWORD** que indica el recuento de elementos de la matriz, seguido de la matriz de elementos.                               |
| Dirección de los datos        | R->I                                                                                                                                                                                                                         |
| Opciones de código de respuesta | **MTP \_ RESPONSE \_ OK** (0x2001) o código de respuesta de error válido.                                                                                                                                                                    |
| Parámetro de respuesta 1  | Identificador de transacción actual.                                                                                                                                                                                                     |
| Parámetro de respuesta 2  | Número de PUOID que quedan por recuperar en solicitudes futuras.                                                                                                                                                            |
| Parámetro de respuesta 3  | **DWORD que** contiene información de estado. El estado se indica de forma bit a bit. Vea Comentarios para obtener información sobre las marcas que se usarán.                                                                                              |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                               |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

El estado se indica a través del parámetro de respuesta 3 bit a bit mediante la marca siguiente.



| Marca                                              | Value | Descripción                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ MARCA LOS ELEMENTOS \_ ADQUIRIDOS NO \_ \_ REPORTADOS** | 0x1   | El dispositivo contiene algunos elementos adquiridos que no se pueden devolver en la lista de PUOIDS. Tenga en cuenta que esta marca no es redundante con el parámetro de respuesta 2. Establezca esta marca solo cuando haya elementos solicitados que el dispositivo no pueda devolver. |



 

Los bits del 1 al 31 están reservados para su uso futuro. Estos bits deben establecerse en cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




