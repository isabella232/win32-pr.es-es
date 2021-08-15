---
description: Los métodos de cursor del mouse permiten a la aplicación especificar un cursor de color proporcionando una superficie que contiene una imagen.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Trabajar con cursores del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518923"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Trabajar con cursores del mouse (Direct3D 9)

Los métodos de cursor del mouse permiten a la aplicación especificar un cursor de color proporcionando una superficie que contiene una imagen. El sistema garantizará que este cursor se actualizará a la mitad de la velocidad de visualización o más si la velocidad de fotogramas de la aplicación es lenta. Sin embargo, el cursor nunca se actualizará con más frecuencia que la frecuencia de actualización de pantalla.

La posición del cursor del mouse está asociada al cursor del sistema, que se escala correctamente para la resolución espacial del modo de presentación actual, pero la aplicación puede moverla explícitamente. Esto es análogo al comportamiento de la API win32: cursor del mouse del sistema admitido. Para obtener más información sobre cómo usar un cursor del mouse en la aplicación Direct3D, consulte los siguientes temas de referencia.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D garantiza que el mouse sea compatible con implementaciones de hardware o con el tiempo de ejecución de Direct3D que realiza operaciones de eliminación acelerada por hardware al llamar a [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
