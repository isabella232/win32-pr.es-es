---
title: Atributos de escucha
description: Atributos de escucha
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Aspectos de Windows Media Player, atributos de escucha
- máscaras, atributos de escucha
- referencia de máscaras, atributos de escucha
- atributos de escucha
- atributos, escuchar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532061"
---
# <a name="listening-attributes"></a>Atributos de escucha

Un atributo de escucha se usa para conectar un atributo a otro, de modo que su valor cambia cada vez que cambia el valor del otro atributo.

El atributo de escucha **wmpprop:** es el más útil. Si se especifica el valor de un atributo para que sea **wmpprop:** de un segundo atributo, el primer valor se actualizará automáticamente para reflejar el segundo valor cada vez que cambie el segundo valor.

**Ejemplo**:


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



De esta manera, el valor de un control deslizante, que se muestra en la posición del control deslizante, también puede mostrarse como un número dentro de un cuadro de texto.

Los otros dos atributos de escucha, **wmpenabled:** y **wmpdisabled:**, se pueden usar para cambiar el atributo **habilitado** de un control en función de si su funcionalidad está actualmente disponible en el reproductor. Estos atributos solo pueden escuchar a los métodos del objeto de **control** .

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

 

 




