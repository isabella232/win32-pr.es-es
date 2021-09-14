---
title: Extensiones de dispositivo MTP para la transferencia de metadatos
description: Extensiones de dispositivo MTP para la transferencia de metadatos
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Reproductor de Windows Media,extensiones de dispositivo MTP
- Reproductor de Windows Media,extensiones de dispositivo
- Reproductor de Windows Media,extensions
- Reproductor de Windows Media,metadata
- Reproductor de Windows Media,Protocolo de transferencia multimedia (MTP)
- Protocolo de transferencia de medios (MTP)
- MTP (protocolo de transferencia de medios)
- metadata,extensiones de dispositivo MTP
- metadata,device extensions
- metadata,extensions
- extensiones de dispositivo, transferencia de metadatos
- extensiones, transferencia de metadatos
- Extensiones de dispositivo MTP para la transferencia de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359281"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Extensiones de dispositivo MTP para la transferencia de metadatos

El Protocolo de transferencia de medios (MTP) es un protocolo diseñado para dispositivos multimedia portátiles. El propósito principal de este protocolo es proporcionar un protocolo común para intercambiar datos entre un equipo y un dispositivo multimedia portátil. Esto incluye recibir y enviar objetos multimedia y enumerar el contenido y las funcionalidades del dispositivo.

MTP usa identificadores de objetos únicos persistentes (PUOID) para identificar de forma única los elementos multimedia digitales (y otros objetos) almacenados en un dispositivo. Al intercambiar información sobre los cambios que se han producido en un dispositivo que admite MTP, el dispositivo y Reproductor de Windows Media usan PUOID para identificar qué objetos han cambiado.

El archivo de encabezado denominado wmpdevices.h, que se instala como parte del SDK de Reproductor de Windows Media, define las estructuras y constantes necesarias para admitir Reproductor de Windows Media extensiones de dispositivo.

Para que un dispositivo se reconozca como compatible con la transferencia de metadatos a través del conjunto de extensiones de dispositivo Reproductor de Windows Media MTP, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo Conjunto de datos          | Orden de campo | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 10.0" |



 

En la tabla siguiente se proporcionan detalles sobre la operación MTP para la transferencia acelerada de metadatos.



| Elemento                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parámetro de operación 1 | Identificador de transacción proporcionado por el dispositivo durante la sesión anterior. Este valor es cero para la primera sesión.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parámetro de operación 2 | Índice inicial. Este valor siempre es cero en la primera llamada de una sesión. En las llamadas posteriores dentro de la misma sesión de sincronización, este valor aumenta por la suma del recuento de los elementos modificados y eliminados de los datos de respuesta anteriores.                                                                                                                                                                                                                                             |
| Parámetro de operación 3 | 0x10000. Esta constante, definida en wmpdevices.h, es el número máximo de PUOID que se pueden devolver en la respuesta. Tenga en cuenta que el valor de esta constante se puede revisar en futuras versiones de este archivo de encabezado.                                                                                                                                                                                                                                                                                     |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Datos                  | El dispositivo devuelve dos matrices MTP contiguas que contienen PUOID. Cada matriz MTP comienza con un **valor DWORD** que indica el recuento de elementos de la matriz, seguido de la matriz de elementos. La primera matriz MTP contiene la lista de PUOID que se han agregado o cambiado. La segunda matriz MTP contiene la lista de PUOID que se han eliminado del dispositivo portátil. Tenga en cuenta que la suma del recuento de PUOID en las dos matrices no debe superar el valor pasado en el parámetro operation 3.<br/> |
| Dirección de datos        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opciones de código de respuesta | **MTP \_ RESPONSE \_ OK** (0x2001) o código de respuesta de error válido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parámetro de respuesta 1  | Identificador de transacción actual del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parámetro de respuesta 2  | Número de PUOID que permanecen para ser recuperados por solicitudes futuras.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parámetro de respuesta 3  | **DWORD que** contiene información de estado. El estado se indica de forma bit a bit. Vea Comentarios para obtener información sobre las marcas que se deben usar.                                                                                                                                                                                                                                                                                                                                                                     |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

El estado se indica a través del parámetro de respuesta 3 de forma bit a bit mediante las marcas siguientes.



| Marca                                             | Value | Descripción                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ MARCA ELEMENTOS \_ ELIMINADOS NO INFORMES \_ \_** | 0x1   | Los elementos se eliminaron antes de que se notificase el primer nombre de ruta de acceso del objeto. Esto a menudo indica que se ha formatear el dispositivo.                                                                                                           |
| **WMP \_ MDRT \_ MARCA ELEMENTOS \_ AGREGADOS NO \_ \_ INFORMES**   | 0x2   | El dispositivo contiene algunos elementos agregados que no se pueden devolver en la lista de PUOIDS. Tenga en cuenta que esta marca no es redundante con el parámetro de respuesta 2. Establezca esta marca solo cuando haya elementos solicitados que el dispositivo no pueda devolver. |



 

Los bits del 2 al 31 se reservan para su uso futuro. Estos bits deben establecerse en cero.

Reproductor de Windows Media envía el comando MTP a un dispositivo al principio de una sesión de sincronización antes de transferir los archivos multimedia. El dispositivo debe devolver su respuesta lo antes posible para evitar retrasos en la operación de sincronización.

Reproductor de Windows Media los valores de los atributos enumerados en Acerca de [los](about-the-metadata.md) metadatos para cada VALOR DE PROPIEDAD modificado devuelto en la respuesta. Reproductor de Windows Media enviar valores actualizados para estos atributos al dispositivo en comandos posteriores.

Los archivos notificados como eliminados del dispositivo se pueden copiar de nuevo en el dispositivo si la configuración del usuario lo requiere.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia acelerada de metadatos**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





