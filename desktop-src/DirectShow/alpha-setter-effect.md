---
description: Efecto de setter alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efecto de setter alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162377"
---
# <a name="alpha-setter-effect"></a>Efecto de setter alfa

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El efecto Alfa Setter establece los bits alfa en una imagen de vídeo.

Identificador de clase (CLSID): {506D89AE-909A-44f7-9444-POSICIÓN575896E35}

Nombre de la variable CLSID: CLSID \_ DxtAlphaSetter

Nombre descriptivo: "DxtAlphaSetter"

### <a name="properties"></a>Propiedades



| Propiedad  | Tipo   | Valor predeterminado | Descripción                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Establece el valor alfa para toda la imagen.                        |
| AlphaRamp | double | -1.0    | Establece el valor alfa como un porcentaje del valor alfa original. |



 

## <a name="remarks"></a>Observaciones

Se omite una propiedad con un valor negativo. Solo una propiedad puede tener un valor no negativo. La propiedad Alpha especifica un valor alfa constante para cada píxel de la imagen. Esta propiedad sobrescribe los valores alfa de la imagen original. La propiedad AlphaRamp especifica el valor alfa de cada píxel como porcentaje del valor original del píxel, de 0,0 a 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



