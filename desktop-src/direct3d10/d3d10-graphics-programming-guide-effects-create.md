---
description: Se crea un efecto cargándolo en el marco de trabajo de efectos.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Crear un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686430"
---
# <a name="create-an-effect-direct3d-10"></a>Crear un efecto (Direct3D 10)

Se crea un efecto cargándolo en el marco de trabajo de efectos. Si el efecto no se ha compilado nunca, se compilará cuando se cree. Los efectos que ya están cargados en la memoria se pueden crear mediante una llamada a [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). En el ejemplo de código siguiente se usa [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) para crear un efecto a partir de un archivo.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



La lectura de un efecto requiere los mismos parámetros que compilar un efecto, más un dispositivo y un grupo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



