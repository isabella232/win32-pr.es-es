---
description: De forma predeterminada, el sistema Direct3D puede escribir en el búfer de profundidad. La mayoría de las aplicaciones dejan la escritura en el búfer de profundidad habilitado, pero puede lograr algunos efectos especiales al no permitir que el sistema Direct3D escriba en el búfer de profundidad.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Cambiar el acceso de escritura del búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0624481518fbc4410fbf1be36acb4e9d7eda80ced7e144e20968f797d91a732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911639"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Cambiar el acceso de escritura del búfer de profundidad (Direct3D 9)

De forma predeterminada, el sistema Direct3D puede escribir en el búfer de profundidad. La mayoría de las aplicaciones dejan la escritura en el búfer de profundidad habilitado, pero puede lograr algunos efectos especiales al no permitir que el sistema Direct3D escriba en el búfer de profundidad.

Puede deshabilitar las escrituras de búfer de profundidad en C++ llamando al método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con el parámetro State establecido en D3DRS ZWRITEENABLE y el parámetro Value establecido en \_ 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
