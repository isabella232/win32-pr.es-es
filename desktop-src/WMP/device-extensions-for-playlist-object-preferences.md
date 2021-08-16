---
title: Extensiones de dispositivo para las preferencias de objetos de lista de reproducción
description: Extensiones de dispositivo para las preferencias de objetos de lista de reproducción
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Reproductor de Windows Media,extensiones de dispositivo
- Reproductor de Windows Media,extensions
- Reproductor de Windows Media,Preferencias de objetos de lista de reproducción
- extensiones de dispositivo, preferencias de objetos de lista de reproducción
- extensiones, preferencias de objeto de lista de reproducción
- Objeto de lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340924"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Extensiones de dispositivo para las preferencias de objetos de lista de reproducción

Como parte del proceso de sincronización, Reproductor de Windows Media 10 o posterior copia objetos de lista de reproducción en dispositivos portátiles habilitados para MTP. Reproductor de Windows Media 11 presenta una nueva funcionalidad que permite a los dispositivos portátiles limitar los tipos de objetos de lista de reproducción copiados. (Reproductor de Windows Media siempre sincroniza el contenido de la lista de reproducción según lo especificado por las reglas de sincronización. Esta característica solo afecta a la sincronización de objetos de lista de reproducción). Reproductor de Windows Media copia tres tipos de objetos de lista de reproducción del equipo al dispositivo:

-   **Listas de reproducción normales.** Se trata de listas de reproducción que están visibles en la **característica Biblioteca** de Reproductor de Windows Media. Estas incluyen listas de reproducción creadas por el usuario, listas de reproducción agregadas a la biblioteca por tiendas en línea y listas de reproducción de ejemplo instaladas con el Reproductor. Reproductor de Windows Media copia solo estas listas de reproducción en el dispositivo cuando el usuario las ha seleccionado para la sincronización.
-   **Listas de reproducción de sincronización de existencias.** Se trata de listas de reproducción especiales que se instalan con Reproductor de Windows Media se usan solo para la sincronización. Estas listas de reproducción solo son visibles en Reproductor de Windows Media device Asistente para instalación.
-   **Listas de reproducción creadas implícitamente.** Estas listas de reproducción se crean cuando el usuario arrastra y coloca una carpeta de categorías, como **Artist** o **Album,** en el panel que muestra los elementos que se van a sincronizar.

El archivo de encabezado denominado wmpdevices.h, que se ha actualizado para esta versión, define las estructuras y constantes necesarias para admitir Reproductor de Windows Media extensiones de dispositivo.

Para que un dispositivo se reconozca como compatible con las preferencias de objeto de lista de reproducción a través del conjunto de extensiones de dispositivo Reproductor de Windows Media MTP, debe incluir la siguiente información en el conjunto de datos DeviceInfo. (Para obtener más información sobre este conjunto de datos, vea la sección 4.6.1 de la especificación de MTP).



| Campo de conjunto de datos          | Orden de los campos | Tipo de datos  | Value                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11.0" |



 

En la tabla siguiente se proporcionan detalles sobre la operación MTP para las preferencias de objetos de lista de reproducción.



| Elemento                  | Descripción                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operación        | 0x9203                                                                                                                                                                                                                                                                                          |
| Parámetro de operación 1 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 2 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 3 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 4 | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de operación 5 | 0                                                                                                                                                                                                                                                                                               |
| Datos                  | El dispositivo devuelve un valor en Parámetro de respuesta 1 para indicar la preferencia de sincronización de objetos de lista de reproducción.                                                                                                                                                                                      |
| Dirección de los datos        | R->I                                                                                                                                                                                                                                                                                         |
| Opciones de código de respuesta | MTP \_ RESPONSE \_ OK (0x2001) o código de respuesta de error válido.                                                                                                                                                                                                                                        |
| Parámetro de respuesta 1  | 0 o 1. Un valor de 0 indica que Reproductor de Windows Media debe sincronizar solo los objetos de lista de reproducción normales. Un valor de 1 indica que ese Reproductor de Windows Media debe sincronizar objetos de lista de reproducción normales, existencias y objetos de lista de reproducción de sincronización creados implícitamente, que es el comportamiento predeterminado. |
| Parámetro de respuesta 2  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 3  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 4  | 0                                                                                                                                                                                                                                                                                               |
| Parámetro de respuesta 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentarios

La implementación de esta característica es opcional para dispositivos portátiles. Reproductor de Windows Media los objetos de lista de reproducción normales, los objetos de lista de reproducción de sincronización de existencias y los objetos de lista de reproducción creados implícitamente de forma predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




