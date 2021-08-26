---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888404"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon::GetEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Recupera el valor de la propiedad [**Enabled para**](enabled-property.md) un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Dirección de una variable que recibe **True cuando** se habilita el globo de palabras y **False** cuando está deshabilitado.

</dd> </dl>

El servidor de Microsoft Agent muestra automáticamente el globo de palabras para la salida hablada, a menos que esté deshabilitado. El globo de palabras se puede deshabilitar para un carácter en el Editor de caracteres de Microsoft Agent o (por el usuario) para todos los caracteres de la hoja de propiedades de Microsoft Agent. Si el usuario deshabilita el globo de palabras, el cliente no puede restaurarlo.

 

 




