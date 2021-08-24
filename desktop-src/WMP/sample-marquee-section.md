---
title: Sección marquesina de ejemplo
description: Sección marquesina de ejemplo
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Reproductor de Windows Media Máscaras móviles, marques
- máscaras, marques
- referencia de máscaras, marques
- marquees en máscaras, sección Marquee
- archivos de definición de máscara, sección Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f8a3e013bb3a09a06f03715f0e7c4914e8e8d344c55843a643d5b8a9bf0479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508125"
---
# <a name="sample-marquee-section"></a>Sección marquesina de ejemplo

En las líneas siguientes se muestra una sección marquesina típica de un archivo de definición de máscara:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Esto define un cuadro de presentación de marquesina que muestra el título y el autor si se definen ambos, el título si solo se define Title o el nombre del autor si solo se define Author. Si no se define ninguno, no se mostrará nada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marquesina**](marquee.md)
</dt> </dl>

 

 




