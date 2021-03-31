---
title: Extensiones de dispositivo MTP para transferencia de metadatos
description: Extensiones de dispositivo MTP para transferencia de metadatos
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player, extensiones de dispositivo MTP
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Media Player de Windows, metadatos
- Windows Media Player, protocolo de transferencia multimedia (MTP)
- Protocolo de transferencia multimedia (MTP)
- MTP (Protocolo de transferencia multimedia)
- metadatos, extensiones de dispositivo MTP
- metadatos, extensiones de dispositivo
- metadatos, extensiones
- extensiones de dispositivo, transferencia de metadatos
- extensiones, transferencia de metadatos
- Extensiones de dispositivo MTP para transferencia de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075046"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Extensiones de dispositivo MTP para transferencia de metadatos

El protocolo de transferencia multimedia (MTP) es un protocolo diseñado para dispositivos multimedia portátiles. El objetivo principal de este protocolo es proporcionar un protocolo común para intercambiar datos entre un equipo y un dispositivo multimedia portátil. Esto incluye la recepción y el envío de objetos multimedia, y la enumeración del contenido y las capacidades del dispositivo.

MTP usa identificadores de objeto únicos (PUOIDs) persistentes para identificar de forma única los elementos multimedia digitales (y otros objetos) almacenados en un dispositivo. Al intercambiar información sobre los cambios que se han producido en un dispositivo que admite MTP, el dispositivo y Windows Media Player usar PUOIDs para identificar qué objetos han cambiado.

El archivo de encabezado denominado wmpdevices. h, que se instala como parte del SDK de Windows Media Player, define las estructuras y constantes necesarias para admitir las extensiones de dispositivo de Windows Media Player.

Para que un dispositivo se reconozca como compatibilidad con la transferencia de metadatos a través del conjunto de extensiones de dispositivo MTP de Windows Media Player, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo de conjunto de los          | Orden de los campos | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 10,0" |



 

En la tabla siguiente se proporcionan detalles sobre la operación MTP para la transferencia de metadatos acelerada.



| Elemento                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parámetro de operación 1 | El ID. de transacción proporcionado por el dispositivo durante la sesión anterior. Este valor es cero para la primera sesión.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parámetro de operación 2 | Índice de inicio. Este valor siempre es cero en la primera llamada de una sesión. En las llamadas posteriores dentro de la misma sesión de sincronización, este valor aumenta en función de la suma del recuento de los elementos modificados y eliminados de los datos de respuesta anteriores.                                                                                                                                                                                                                                             |
| Parámetro de operación 3 | 0x10000. Esta constante, definida en wmpdevices. h, es el número máximo de PUOIDs que se puede devolver en la respuesta. Tenga en cuenta que el valor de esta constante se puede revisar en futuras versiones de este archivo de encabezado.                                                                                                                                                                                                                                                                                     |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Datos                  | El dispositivo devuelve dos matrices MTP contiguas que contienen PUOIDs. Cada matriz MTP comienza con un valor **DWORD** que indica el recuento de elementos de la matriz, seguido de la matriz de elementos. La primera matriz MTP contiene la lista de PUOIDs que se han agregado o cambiado. La segunda matriz MTP contiene la lista de PUOIDs que se han eliminado del dispositivo portátil. Tenga en cuenta que la suma del recuento de PUOID en las dos matrices no debe superar el valor pasado en el parámetro de operación 3.<br/> |
| Dirección de datos        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opciones de código de respuesta | **MTP \_ RESPUESTA \_ correcta** (0x2001) o código de respuesta de error válido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parámetro de respuesta 1  | El identificador de la transacción actual del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parámetro de respuesta 2  | El número de PUOIDs que quedan para ser recuperadas por solicitudes futuras.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parámetro de respuesta 3  | **DWORD** que contiene información de estado. El estado se indica de forma bit a bit. Vea la sección Comentarios para obtener información sobre las marcas que se deben usar.                                                                                                                                                                                                                                                                                                                                                                     |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

El estado se indica a través del parámetro de respuesta 3 de manera bit a bit mediante el uso de las marcas siguientes.



| Marca                                             | Value | Descripción                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ marca \_ \_ los elementos eliminados no notificados \_** | 0x1   | Los elementos se eliminaron antes de que se notifique el primer nombre de ruta de acceso al objeto. Esto suele indicar que se ha cambiado el formato del dispositivo.                                                                                                           |
| **WMP \_ MDRT \_ marca \_ \_ elementos agregados no notificados \_**   | 0x2   | El dispositivo contiene algunos elementos agregados que no se pueden devolver en la lista de PUOIDS. Tenga en cuenta que esta marca no es redundante con el parámetro de respuesta 2. Establezca esta marca solo cuando haya elementos solicitados que el dispositivo no pueda devolver. |



 

Los bits 2 a 31 se reservan para uso futuro. Estos bits deben establecerse en cero.

Windows Media Player envía el comando MTP a un dispositivo al inicio de una sesión de sincronización antes de que se transfieran los archivos multimedia. El dispositivo debe devolver su respuesta lo más rápido posible para evitar retrasos en la operación de sincronización.

Windows Media Player solicitará valores para los atributos que se enumeran en [acerca de los metadatos](about-the-metadata.md) de cada POUID modificado devuelto en la respuesta. Windows Media Player podría enviar valores actualizados para estos atributos al dispositivo en comandos posteriores.

Los archivos que se notifiquen como que se han quitado del dispositivo pueden volver a copiarse en el dispositivo si la configuración del usuario lo requiere.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia de metadatos acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





