---
title: Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows
description: Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Administrador de dispositivos, reproductores de audio portátiles
- Administrador de dispositivos, reproductores de audio portátiles
- Guía de programación, reproductores de audio portátiles
- proveedores de servicios, reproductores de audio portátiles
- creación de proveedores de servicios, reproductores de audio portátiles
- reproductores de audio portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695336"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows

La extensión de espacio de nombres del shell del reproductor de audio portátil proporciona a los usuarios de Windows una manera coherente de administrar los dispositivos de audio administrados por Administrador de dispositivos de Windows Media. Si crea los componentes del proveedor de servicios y del controlador según las siguientes directrices, el dispositivo se mostrará en el espacio de nombres del shell. Los usuarios podrán interactuar con el contenido del dispositivo de forma coherente en el explorador de Windows para realizar operaciones básicas, como copiar, eliminar y cambiar el nombre.

Los siguientes requisitos de Shell para el proveedor de servicios y los componentes de controlador están diseñados para complementar las directrices generales de Windows Media Administrador de dispositivos.

Capacidades del dispositivo

Los proveedores de servicios de Windows Media Administrador de dispositivos deben ser explícitos en sus capacidades admitidas. Si no se admite una llamada, se debe devolver un código de error. Se deben establecer los campos adecuados para la presencia o ausencia de funcionalidades en la devolución de las siguientes funciones:

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Los proveedores de servicios deben admitir las siguientes funcionalidades para ser compatibles con el Shell:

-   Copiar en el dispositivo (compatible con las devoluciones de llamada de cancelación y progreso)
-   Eliminar archivo del dispositivo (compatible con las devoluciones de llamada de cancelación y progreso)
-   Cambiar el nombre del archivo en el dispositivo
-   Informes de espacio (espacio total, espacio libre, espacio inutilizable)
-   Plug and Play (consulte [habilitación de PNP para dispositivos](enabling-pnp-for-devices.md))
-   Formato (preferiblemente con compatibilidad con las devoluciones de llamada de cancelación y progreso)

Si se admiten metadatos, se deben admitir los siguientes campos para archivos individuales. Si no hay datos disponibles, el campo debe inicializarse como una cadena vacía:



| Campo        | Constante (definida en WMDM. idl) | Etiqueta Metadata    |
|--------------|--------------------------------|-----------------|
| Título de la canción   | g \_ wszWMDMTitle                | WMDM/título      |
| Número de pista | g \_ wszWMDMTrack                | WMDM/Track      |
| Artistas       | g \_ wszWMDMAuthor               | WMDM/autor     |
| Álbum        | g \_ wszWMDMAlbumTitle           | WMDM/álbum |
| Year         | g \_ wszWMDMYear                 | WMDM/año       |
| Género        | g \_ wszWMDMGenre                | WMDM/género      |



 

Simultaneidad

Los controladores de modo kernel para Windows Media Administrador de dispositivos deben ser sólidos para controlar el acceso simultáneo. Por ejemplo, un usuario puede tener acceso simultáneamente al dispositivo a través del shell y el reproductor multimedia, o simplemente a través de varias ventanas en el shell. Como parte del control de la simultaneidad, los controladores no deben asumir, solo porque se ha cargado el proveedor de servicios, que el dispositivo está en uso. En su lugar, deben implementar un mecanismo de bloqueo para serializar el acceso al dispositivo según sea necesario para las operaciones individuales.

UI

Los proveedores de servicios de Windows Media Administrador de dispositivos no deben mostrar ninguna interfaz de usuario. Siempre que sea posible, se deben devolver todos los errores de las llamadas de método como códigos de error específicos de Windows Media Administrador de dispositivos.

Habilitar en el shell

Si el paquete cumple todos los requisitos de Shell, puede habilitar el dispositivo para que se muestre en el shell estableciendo el valor de *ShowInShell* en 1 en los parámetros del dispositivo. Para obtener más información, vea [parámetros de dispositivo](device-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




