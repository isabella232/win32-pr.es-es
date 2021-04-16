---
description: Los métodos de cursor del mouse permiten que la aplicación especifique un cursor de color proporcionando una superficie que contenga una imagen.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Trabajar con cursores del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495563"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Trabajar con cursores del mouse (Direct3D 9)

Los métodos de cursor del mouse permiten que la aplicación especifique un cursor de color proporcionando una superficie que contenga una imagen. El sistema garantizará que este cursor se actualizará a la mitad de la velocidad de presentación o más si la velocidad de fotogramas de la aplicación es lenta. Sin embargo, el cursor nunca se actualizará con más frecuencia que la frecuencia de actualización de la pantalla.

La posición del cursor del mouse está ligada al cursor del sistema, escalada correctamente para la resolución espacial del modo de presentación actual, pero la aplicación puede moverla explícitamente. Esto es análogo al comportamiento del cursor del mouse del sistema compatible con la API Win32. Para obtener más información sobre cómo usar un cursor del mouse en la aplicación Direct3D, vea los temas de referencia siguientes.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D garantiza que el mouse es compatible con las implementaciones de hardware o con el tiempo de ejecución de Direct3D que realiza operaciones de blitting aceleradas por hardware al llamar a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
