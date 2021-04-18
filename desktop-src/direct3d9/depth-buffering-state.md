---
description: El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas. De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Estado de almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494920"
---
# <a name="depth-buffering-state-direct3d-9"></a>Estado de almacenamiento en búfer de profundidad (Direct3D 9)

El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas. De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.

Para obtener información general conceptual de los búferes de profundidad, vea [búferes de profundidad (Direct3D 9)](depth-buffers.md).

Las aplicaciones de C++ actualizan el estado de almacenamiento en búfer de profundidad con el \_ Estado de representación de ZENABLE de D3DRS, mediante un miembro de la enumeración [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) para especificar el nuevo valor de estado.

Si la aplicación necesita impedir que Direct3D escriba en el búfer de profundidad, puede usar el \_ valor enumerado D3DRS ZWRITEENABLE, especificando D3DZB \_ false como el segundo parámetro para la llamada a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En el ejemplo de código siguiente se muestra cómo se establece el estado del búfer de profundidad para habilitar el almacenamiento en búfer z.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



La aplicación también puede usar el estado de representación de D3DRS \_ ZFUNC para controlar la función de comparación que usa Direct3D al realizar el almacenamiento en búfer de profundidad.

La inclinación de Z es un método para mostrar una superficie delante de otra, incluso si sus valores de profundidad son los mismos. Puede utilizar esta técnica para diversos efectos. Un ejemplo común es la representación de sombras en las paredes. Tanto la sombra como la pared tienen el mismo valor de profundidad. Sin embargo, desea que la aplicación muestre la sombra en la pared. La asignación de una diferencia de z a la sombra hace que Direct3D las muestre correctamente (consulte D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
