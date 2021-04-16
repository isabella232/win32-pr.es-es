---
description: La propiedad PlayState recupera el estado actual del objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propiedad PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686338"
---
# <a name="playstate-property"></a>Propiedad PlayState

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `PlayState` propiedad recupera el estado actual del objeto **MSWebDVD** .

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el estado actual del navegador del DVD.



| Código devuelto | Descripción   |
|-------------|---------------|
| -2          | No definido     |
| -1          | No inicializado |
| 0           | Detenido       |
| 1           | En pausa        |
| 2           | En ejecución       |



 

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.

El objeto **MSWebDVD** controla el filtro de navegador de DVD de DirectShow, que realiza el trabajo real de la navegación por DVD. En realidad, es el estado del navegador de DVD al que hace referencia esta propiedad. El navegador de DVD puede estar en uno de varios Estados, tal y como se ha descrito anteriormente. La `PlayState` propiedad puede ser útil como herramienta de diagnóstico, pero generalmente no debería haber ninguna razón para que una aplicación de scripts supervise el estado del navegador del DVD.

 

 



