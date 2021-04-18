---
description: De forma predeterminada, se permite que el sistema Direct3D escriba en el búfer de profundidad. La mayoría de las aplicaciones dejan de escribir en el búfer de profundidad habilitado, pero puede conseguir algunos efectos especiales si no permite que el sistema Direct3D escriba en el búfer de profundidad.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Cambiar el acceso de escritura de búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714826"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Cambiar el acceso de escritura de búfer de profundidad (Direct3D 9)

De forma predeterminada, se permite que el sistema Direct3D escriba en el búfer de profundidad. La mayoría de las aplicaciones dejan de escribir en el búfer de profundidad habilitado, pero puede conseguir algunos efectos especiales si no permite que el sistema Direct3D escriba en el búfer de profundidad.

Puede deshabilitar las escrituras de búfer de profundidad en C++ llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con el parámetro State establecido en D3DRS \_ ZWRITEENABLE y el parámetro value establecido en 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
