---
description: Efecto del establecedor alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efecto del establecedor alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805929"
---
# <a name="alpha-setter-effect"></a>Efecto del establecedor alfa

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El efecto establecedor alfa establece los bits alfa de una imagen de vídeo.

IDENTIFICADOR de clase (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}

Nombre de la variable CLSID: CLSID \_ DxtAlphaSetter

Nombre descriptivo: "DxtAlphaSetter"

### <a name="properties"></a>Propiedades



| Propiedad  | Tipo   | Valor predeterminado | Descripción                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Establece el alfa de la imagen completa.                        |
| AlphaRamp | double | -1.0    | Establece el alfa como porcentaje del valor alfa original. |



 

## <a name="remarks"></a>Observaciones

Se omite una propiedad con un valor negativo. Solo una propiedad puede tener un valor no negativo. La propiedad alfa especifica un valor alfa constante para cada píxel de la imagen. Esta propiedad sobrescribe los valores alfa de la imagen original. La propiedad AlphaRamp especifica el valor alfa de cada píxel como un porcentaje del valor original del píxel, de 0,0 a 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 



