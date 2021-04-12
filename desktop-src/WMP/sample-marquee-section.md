---
title: Sección de marquesina de ejemplo
description: Sección de marquesina de ejemplo
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, sección de marquesina
- archivos de definición de máscara, sección de marquesina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486963"
---
# <a name="sample-marquee-section"></a>Sección de marquesina de ejemplo

Las siguientes líneas muestran una sección de marquesina típica de un archivo de definición de máscara:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Esto define un cuadro de presentación de marquesina que muestra el título y el autor si ambos están definidos, el título si solo se define el título o el nombre del autor si solo se define Author. Si no se define ninguno, no se mostrará nada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marquesina**](marquee.md)
</dt> </dl>

 

 




