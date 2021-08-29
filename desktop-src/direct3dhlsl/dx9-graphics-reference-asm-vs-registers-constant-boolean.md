---
title: Registro booleano constante (referencia de HLSL VS)
description: Este registro es una colección de bits usados en instrucciones de control de flujo estático (por ejemplo, si bool - vs - else - vs - endif - vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d99dc4d11c5886b6d6905bd8b612654f46e5726215edfe32353062df4d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982785"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a>Registro booleano constante (referencia de HLSL VS)

Este registro es una colección de bits que se usan en las instrucciones de control de flujo estático (por ejemplo, [si bool - vs](if-bool---vs.md)else -  -  [vs](else---vs.md)  -  [endif - vs](endif---vs.md)). Hay 16, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes. Se pueden establecer mediante [defb - vs o](defb---vs.md) [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).

El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.

-   Para Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador. La duración de una constante declarada con defx solo se limita a la ejecución de ese sombreador. Por el contrario, las constantes establecidas mediante las API SetXXXShaderConstantX inicializan constantes en el espacio global. Las constantes del espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.
-   Para Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador. Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes, independientemente de la técnica utilizada para establecerlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 