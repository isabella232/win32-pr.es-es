---
title: Requisitos para que los reproductores de audio portátiles aparezcan en Windows Explorer
description: Requisitos para que los reproductores de audio portátiles aparezcan en Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Reproductores Administrador de dispositivos multimedia, reproductores de audio portátiles
- Administrador de dispositivos, reproductores de audio portátiles
- guía de programación, reproductores de audio portátiles
- proveedores de servicios, reproductores de audio portátiles
- crear proveedores de servicios, reproductores de audio portátiles
- reproductores de audio portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d91e844f564ead03ddb78cf57c13c81a56bc8934bbfbde51c105b5c7e1e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055583"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisitos para que los reproductores de audio portátiles aparezcan en Windows Explorer

La extensión de espacio de nombres de shell del reproductor de audio portátil proporciona a Windows usuarios una manera coherente de administrar dispositivos de audio administrados por Windows Media Administrador de dispositivos. Si cree el proveedor de servicios y los componentes del controlador según las siguientes directrices, el dispositivo se mostrará en el espacio de nombres del shell. Los usuarios podrán interactuar con el contenido del dispositivo de forma coherente en Windows Explorer para realizar operaciones básicas como copiar, eliminar y cambiar el nombre.

Los siguientes requisitos de shell para los componentes de controlador y proveedor de servicios están diseñados para complementar las directrices generales Windows de Administrador de dispositivos multimedia.

Capacidades del dispositivo

Windows Los Administrador de dispositivos de servicios multimedia deben ser explícitos en sus funcionalidades admitidas. Si no se admite una llamada, se debe devolver un código de error. Se deben establecer los campos adecuados para la presencia o ausencia de funcionalidades a la hora de devolver las siguientes funciones:

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Los proveedores de servicios deben admitir las siguientes funcionalidades para que sean compatibles con el shell:

-   Copiar en el dispositivo (con compatibilidad con devoluciones de llamada de cancelación y progreso)
-   Eliminación de un archivo del dispositivo (compatible con las devoluciones de llamada de cancelación y progreso)
-   Cambiar el nombre del archivo en el dispositivo
-   Informes de espacio (espacio total, espacio libre, espacio inutilizable)
-   Plug and Play (consulte [Habilitación de PnP para dispositivos)](enabling-pnp-for-devices.md)
-   Formato (preferiblemente compatible con devoluciones de llamada de cancelación y progreso)

Si se admiten metadatos, los siguientes campos deben ser compatibles con archivos individuales. Si no hay datos disponibles, el campo debe inicializarse como una cadena vacía:



| Campo        | Constante (definida en WMDM.idl) | Etiqueta de metadatos    |
|--------------|--------------------------------|-----------------|
| Título de la canción   | g \_ wszWMDMTitle                | WMDM/Title      |
| Número de seguimiento | g \_ wszWMDMTrack                | WMDM/Track      |
| Artista       | g \_ wszWMDMAuthor               | WMDM/Author     |
| Álbum        | g \_ wszWMDMAlbumTitle           | WMDM/AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/Year       |
| Género        | g \_ wszWMDMGenre                | WMDM/Genre      |



 

Simultaneidad

Los controladores de modo kernel Windows media Administrador de dispositivos deben ser sólidos para controlar el acceso simultáneo. Por ejemplo, un usuario puede tener acceso simultáneamente al dispositivo a través del shell y el reproductor multimedia o simplemente a través de varias ventanas del shell. Como parte del control de la simultaneidad, los controladores no deben asumir, simplemente porque se carga el proveedor de servicios, que el dispositivo está en uso. En su lugar, deben implementar un mecanismo de bloqueo para serializar el acceso al dispositivo según sea necesario para operaciones individuales.

UI

Los proveedores de servicios Windows media Administrador de dispositivos no deben mostrar ninguna interfaz de usuario. Los errores deben devolverse desde llamadas de método como códigos de error Windows media Administrador de dispositivos código de error.

Habilitación en el shell

Si el paquete cumple todos los requisitos del shell, puede permitir que el dispositivo se muestre en el shell estableciendo el valor de *ShowInShell* en 1 en los parámetros del dispositivo. Para más información, consulte Parámetros [del dispositivo.](device-parameters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




