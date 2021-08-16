---
title: Registro de color
description: Estos registros de salida del sombreador de vértices contienen un valor de color.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512291"
---
# <a name="color-register"></a>Registro de color

Estos registros de salida del sombreador de vértices contienen un valor de color. 

| Registrarse | Descripción              |
|----------|--------------------------|
| oD0      | registro de color difuso.  |
| oD1      | registro de color especular. |



 

El valor de oD0 está interpolado y se escribe en el registro de color del sombreador de píxeles 0 (v0). El valor de oD1 se interpola y se escribe en el registro de color del sombreador de píxeles 1 (v1). Para obtener más información sobre los registros de color del sombreador de píxeles, vea el tema Registro de [color de entrada del](dx9-graphics-reference-asm-ps-registers-input-color.md) sombreador de píxeles.

## <a name="remarks"></a>Comentarios

Ejemplo


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




