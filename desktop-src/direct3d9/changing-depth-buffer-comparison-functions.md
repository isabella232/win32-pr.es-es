---
description: De forma predeterminada, cuando se realiza la prueba de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de representación y destino si el valor de profundidad correspondiente (z o w) de cada punto es menor que el valor del búfer de profundidad.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Cambiar las funciones de comparación de búfer de profundidad (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807946"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Cambiar las funciones de comparación de búfer de profundidad (D3D9)

De forma predeterminada, cuando se realiza la prueba de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de representación y destino si el valor de profundidad correspondiente (z o w) de cada punto es menor que el valor del búfer de profundidad. En una aplicación de C++, se cambia el modo en que el sistema realiza comparaciones en valores de profundidad llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) con el parámetro de *Estado* establecido en D3DRS \_ ZFUNC. El parámetro *Value* debe establecerse en un valor en el tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
