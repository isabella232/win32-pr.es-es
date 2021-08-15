---
description: Muchas aplicaciones de C++ borran el búfer de profundidad antes de representar cada fotograma nuevo.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Borrar búferes de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989315"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Borrar búferes de profundidad (Direct3D 9)

Muchas aplicaciones de C++ borran el búfer de profundidad antes de representar cada fotograma nuevo. Puede borrar explícitamente el búfer de profundidad a través de Direct3D llamando a [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) y especificando D3DCLEAR ZBUFFER para el \_ parámetro Flags. El **método IDirect3DDevice9::Clear** permite especificar un valor de profundidad arbitrario en el parámetro Z.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
