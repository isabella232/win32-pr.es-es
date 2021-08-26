---
description: 'Las aplicaciones de Direct3D se pueden ejecutar en cualquiera de estos dos modos: a pantalla completa o en ventanas.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modo de ventana Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a845c464e6c402c46cc4aff09196ccfde65ad90371187045b0c14c41315a9f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025755"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Modo de ventana Full-Screen (Direct3D 9)

Las aplicaciones de Direct3D se pueden ejecutar en cualquiera de estos dos modos: a pantalla completa o en ventanas.

El modo de pantalla completa significa que la ventana en la que se ejecuta la aplicación cubre todo el escritorio, ocultando todas las aplicaciones en ejecución (incluido el entorno de desarrollo). Normalmente, los juegos tienen como valor predeterminado el modo de pantalla completa para adentrar completamente al usuario en el juego ocultando todas las aplicaciones en ejecución. Una aplicación que se ejecuta en modo de ventana comparte el escritorio con todas las aplicaciones en ejecución. Las diferencias de código entre el modo de pantalla completa y el modo de ventana son muy pequeñas.

Dado que una aplicación que se ejecuta en modo de pantalla completa toma el control de la pantalla, la depuración de la aplicación requiere un monitor independiente o el uso de un depurador remoto. Use [directX Panel de control Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) para habilitar la depuración de varios monitores. Una ventaja de una aplicación en modo de ventana es que puede pasar por el código de un depurador sin varios monitores ni un depurador remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



