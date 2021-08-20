---
title: Atributos de escucha
description: Atributos de escucha
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Reproductor de Windows Media máscaras, atributos de escucha
- máscaras, atributos de escucha
- referencia de máscaras, atributos de escucha
- atributos de escucha
- attributes,listening
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cceb9a8721995c494b5e4366291353376a2569c045e41eb41c1418e2f4d5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996415"
---
# <a name="listening-attributes"></a>Atributos de escucha

Un atributo de escucha se usa para conectar un atributo a otro para que su valor cambie cada vez que cambia el valor del otro atributo.

El atributo de **escucha wmpprop:** es el más útil. Si se especifica que el valor de un atributo es **wmpprop:** de un segundo atributo, el primer valor se actualizará automáticamente para reflejar el segundo valor cada vez que cambie el segundo valor.

**Ejemplo**:


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



De este modo, el valor de mySlider, mostrado por la posición del control deslizante, también se puede mostrar como un número dentro de un cuadro de texto.

Los otros dos atributos de escucha, **wmpenabled:** y **wmpdisabled:**, se pueden usar para cambiar el atributo habilitado de un control en función de si su funcionalidad está disponible actualmente en el reproductor.  Estos atributos solo pueden escuchar a los métodos del **objeto Controls.**

**Ejemplo**:


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Varios**](miscellaneous.md)
</dt> </dl>

 

 




