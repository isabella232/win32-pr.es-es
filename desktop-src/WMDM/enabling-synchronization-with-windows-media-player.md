---
title: Habilitación de la sincronización con Reproductor de Windows Media
description: Habilitación de la sincronización con Reproductor de Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Administrador de dispositivos,synchronization with Reproductor de Windows Media
- Administrador de dispositivos,sincronización con Reproductor de Windows Media
- guía de programación, sincronización con Reproductor de Windows Media
- proveedores de servicios, sincronización con Reproductor de Windows Media
- crear proveedores de servicios, sincronización con Reproductor de Windows Media
- sincronización con Reproductor de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef06dd0e32e0ea95674f54b94336ecb6882e8215775c857ee0780a58b71af75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585013"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Habilitación de la sincronización con Reproductor de Windows Media

Puede permitir que un dispositivo participe en la sincronización automática con Reproductor de Windows Media. La sincronización automática significa que cuando un dispositivo sincronizado designado por el usuario se conecta al equipo, Reproductor de Windows Media descargará, actualizará o eliminará automáticamente los archivos del dispositivo sin necesidad de ninguna entrada de usuario adicional.

De forma predeterminada, los siguientes dispositivos se sincronizan con Reproductor de Windows Media:

-   Dispositivos MTP
-   Dispositivos de almacenamiento masivo
-   Windows CE dispositivos (Reproductor de Windows Media 10 Mobile y versiones posteriores)

Para que cualquier otro dispositivo se sincronice con Reproductor de Windows Media, deben cumplirse los siguientes requisitos:

-   El dispositivo debe anunciar una interfaz de dispositivo PAP que sea {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Los objetos de dispositivo devueltos por el proveedor de servicios deben admitir la **interfaz IMDSPDevice3.**
-   El parámetro de dispositivo UseExtendedWmdm debe establecerse en un **valor DWORD** de 1. Consulte [Parámetros del dispositivo](device-parameters.md) para obtener más información.
-   El proveedor de servicios debe implementar las interfaces siguientes:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> <dt>

[**Parámetros del dispositivo**](device-parameters.md)
</dt> </dl>

 

 




