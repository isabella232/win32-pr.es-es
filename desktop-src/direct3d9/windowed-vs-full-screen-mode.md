---
description: 'Las aplicaciones de Direct3D pueden ejecutarse en cualquiera de los dos modos: pantalla completa o con ventanas.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modo de ventana de vs Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152112"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Modo de ventana de vs Full-Screen (Direct3D 9)

Las aplicaciones de Direct3D pueden ejecutarse en cualquiera de los dos modos: pantalla completa o con ventanas.

El modo de pantalla completa significa que la ventana en la que se ejecuta la aplicación abarca todo el escritorio, ocultando todas las aplicaciones en ejecución (incluido el entorno de desarrollo). Normalmente, los juegos tienen como valor predeterminado el modo de pantalla completa para sumergir completamente al usuario en el juego ocultando todas las aplicaciones en ejecución. Una aplicación que se ejecuta en modo de ventana comparte el escritorio con todas las aplicaciones en ejecución. Las diferencias de código entre el modo de pantalla completa y el modo de ventana son muy pequeñas.

Dado que una aplicación que se ejecuta en el modo de pantalla completa ocupa la pantalla, la depuración de la aplicación requiere un monitor independiente o el uso de un depurador remoto. Use la [herramienta panel de control de DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) para habilitar la depuración de varios monitores. Una de las ventajas de una aplicación en modo de ventana es que puede recorrer paso a paso el código en un depurador sin varios monitores o un depurador remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



