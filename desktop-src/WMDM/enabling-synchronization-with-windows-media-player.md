---
title: Habilitar la sincronización con Windows Media Player
description: Habilitar la sincronización con Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Administrador de dispositivos, sincronización con Windows Media Player
- Administrador de dispositivos, sincronización con Media Player de Windows
- Guía de programación, sincronización con Windows Media Player
- proveedores de servicios, sincronización con Windows Media Player
- crear proveedores de servicios, sincronización con Windows Media Player
- sincronización con Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695486"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Habilitar la sincronización con Windows Media Player

Puede habilitar un dispositivo para que participe en la sincronización automática con Windows Media Player. La sincronización automática significa que cuando un dispositivo sincronizado designado por el usuario se conecta al equipo, Windows Media Player descargará, actualizará o eliminará automáticamente archivos del dispositivo sin necesidad de proporcionar ninguna entrada adicional por parte del usuario.

De forma predeterminada, los siguientes dispositivos están sincronizados con Windows Media Player:

-   Dispositivos MTP
-   Dispositivos de almacenamiento masivo
-   Dispositivos Windows CE (Windows Media Player 10 Mobile y versiones posteriores)

Para que cualquier otro dispositivo se sincronice con Windows Media Player, deben cumplirse los siguientes requisitos:

-   El dispositivo debe anunciar una interfaz de dispositivo PAP {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Los objetos de dispositivo devueltos por el proveedor de servicios deben admitir la interfaz **IMDSPDevice3** .
-   El parámetro de dispositivo UseExtendedWmdm debe establecerse en un valor **DWORD** de 1. Consulte [parámetros del dispositivo](device-parameters.md) para obtener más información.
-   El proveedor de servicios debe implementar las siguientes interfaces:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> <dt>

[**Parámetros del dispositivo**](device-parameters.md)
</dt> </dl>

 

 




