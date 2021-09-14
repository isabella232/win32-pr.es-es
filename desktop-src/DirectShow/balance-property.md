---
description: La propiedad Balance establece o recupera el equilibrio del altavoz para la salida de la secuencia de audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propiedad Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161701"
---
# <a name="balance-property"></a>Propiedad Balance

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `Balance` propiedad establece o recupera el equilibrio del altavoz para la salida de la secuencia de audio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa los niveles de equilibrio. El intervalo de entrada permitido es de -10 000 a 10 000. Un valor de 0 establece un equilibrio neutro, es decir, los altavoces izquierdo y derecho reciben la misma señal de audio de amplitud.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de 0, lo que significa que ambos hablantes reciben señales de audio equivalentes. Al igual que [**con la propiedad Volume,**](volume-property.md) las unidades corresponden a decibelios .01 (multiplicados por -1 cuando


```
iBalance
```



es un valor positivo). Por ejemplo, un valor de 1000 indica 10 dB en el canal derecho y 90 dB en el canal izquierdo.

 

 



