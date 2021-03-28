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
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104361773"
---
# <a name="color-register"></a>Registro de color

Estos registros de salida del sombreador de vértices contienen un valor de color. 

| Registrarse | Descripción              |
|----------|--------------------------|
| oD0      | registro de color difuso.  |
| oD1      | registro de color especular. |



 

El valor oD0 se interpola y se escribe en el registro de color del sombreador de píxeles 0 (V0). El valor oD1 se interpola y se escribe en el registro de color del sombreador de píxeles 1 (V1). Para obtener más información sobre los registros de color del sombreador de píxeles, vea el tema [registro del color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) del sombreador de píxeles.

## <a name="remarks"></a>Comentarios

Ejemplo


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




