---
title: Extensiones de dispositivo para preferencias de objetos de lista de reproducción
description: Extensiones de dispositivo para preferencias de objetos de lista de reproducción
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Windows Media Player, preferencias de objetos de lista de reproducción
- extensiones de dispositivo, preferencias de objetos de lista de reproducción
- extensiones, preferencias del objeto de lista de reproducción
- Objeto Playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd9c6301e33307fc49e50b8aa9042752e020e32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778270"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Extensiones de dispositivo para preferencias de objetos de lista de reproducción

Como parte del proceso de sincronización, Windows Media Player 10 o posterior copia los objetos de la lista de reproducción en dispositivos portátiles habilitados para MTP. Windows Media Player 11 presenta una nueva funcionalidad que permite a los dispositivos portátiles limitar los tipos de objetos de lista de reproducción que se copian. (Windows Media Player siempre sincroniza el contenido de la lista de reproducción según lo especificado en las reglas de sincronización. Esta característica solo afecta a la sincronización de objetos de lista de reproducción). Windows Media Player copia tres tipos de objetos de lista de reproducción del equipo al dispositivo:

-   **Listas de reproducción ordinarias.** Se trata de listas de reproducción que son visibles en la característica de **biblioteca** de Windows Media Player. Entre ellas se incluyen listas de reproducción creadas por el usuario, listas de reproducción agregadas a la biblioteca por tiendas en línea y listas de reproducción de ejemplo instaladas con el reproductor. Windows Media Player copia solo estas listas de reproducción en el dispositivo cuando el usuario las ha seleccionado para la sincronización.
-   **Listas de reproducción de la sincronización de existencias.** Se trata de listas de reproducción especiales que se instalan con Windows Media Player y que solo se usan para la sincronización. Estas listas de reproducción solo están visibles en el Asistente para la instalación de Windows Media Player Device.
-   **Listas de reproducción creadas implícitamente.** Estas listas de reproducción se crean cuando el usuario arrastra y coloca una carpeta de categorías, como **artista** o **álbum**, en el panel que muestra los elementos que se van a sincronizar.

El archivo de encabezado denominado wmpdevices. h, que se ha actualizado para esta versión, define las estructuras y las constantes necesarias para admitir las extensiones de dispositivo de Windows Media Player.

Para que un dispositivo se reconozca como compatible con las preferencias del objeto de lista de reproducción a través del conjunto de extensiones de dispositivo MTP de Windows Media Player, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo de conjunto de los          | Orden de los campos | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11,0" |



 

En la tabla siguiente se proporcionan detalles acerca de la operación MTP para las preferencias del objeto de lista de reproducción.



| Elemento                  | Descripción                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9203                                                                                                                                                                                                                                                                                          |
| Parámetro de operación 1 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 2 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 3 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                                                                                               |
| Datos                  | El dispositivo devuelve un valor en el parámetro de respuesta 1 para indicar la preferencia de sincronización del objeto de lista de reproducción.                                                                                                                                                                                      |
| Dirección de datos        | R->I                                                                                                                                                                                                                                                                                         |
| Opciones de código de respuesta | \_Respuesta MTP \_ correcta (0x2001) o código de respuesta de error válido.                                                                                                                                                                                                                                        |
| Parámetro de respuesta 1  | 0 o 1. Un valor de 0 indica que Windows Media Player debe sincronizar solo los objetos de listas de reproducción normales. Un valor de 1 indica que Windows Media Player debe sincronizar los objetos de lista de reproducción ordinarios, las existencias y los objetos de lista de reproducción de sincronización creados implícitamente, que es el comportamiento predeterminado. |
| Parámetro de respuesta 2  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 3  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

La implementación de esta característica es opcional para dispositivos portátiles. Windows Media Player sincroniza los objetos de listas de reproducción normales, los objetos de lista de reproducción de la sincronización de existencias y los objetos de lista de reproducción creados implícitamente de forma predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




