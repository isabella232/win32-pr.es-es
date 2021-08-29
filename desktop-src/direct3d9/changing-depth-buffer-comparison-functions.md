---
description: De forma predeterminada, cuando se realizan pruebas de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de destino de representación si el valor de profundidad correspondiente (z o w) para cada punto es menor que el valor del búfer de profundidad.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Cambiar funciones de comparación de búfer de profundidad (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbb808b84fd95eb36e3ea66c4e6faf882826faf8a8c2ab3ed3b9b06f9da79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989325"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Cambiar funciones de comparación de búfer de profundidad (D3D9)

De forma predeterminada, cuando se realizan pruebas de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de destino de representación si el valor de profundidad correspondiente (z o w) para cada punto es menor que el valor del búfer de profundidad. En una aplicación de C++, se cambia el modo en que el sistema realiza comparaciones en los valores de profundidad mediante una llamada al método [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) con el parámetro *State* establecido en D3DRSRENDERUNC. \_ El *parámetro Value* debe establecerse en un valor del tipo enumerado [**D3DCMPFUNC.**](./d3dcmpfunc.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
