---
description: Se crea un efecto al cargarlo en el marco de efectos.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Crear un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75014688c62e6f8f0463c430b0b17aafd28e0ad3764d00b8a357a6613565d87d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567065"
---
# <a name="create-an-effect-direct3d-10"></a>Crear un efecto (Direct3D 10)

Se crea un efecto al cargarlo en el marco de efectos. Si el efecto nunca se ha compilado, se compilará cuando se cree. Los efectos que ya están cargados en la memoria se pueden crear llamando a [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). En el ejemplo de código siguiente se [**usa D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) para crear un efecto a partir de un archivo.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



La lectura de un efecto requiere los mismos parámetros que la compilación de un efecto, además de un dispositivo y un grupo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



