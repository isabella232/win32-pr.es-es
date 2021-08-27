---
description: El método Step avanza el DVD-Video secuencia según el número de fotogramas especificado.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Método Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5738e8704b24d64a429d8d38f1b9eac2f9b8ff7e22a7e9d1d2a29fb9df4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050315"
---
# <a name="step-method"></a>Método Step

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Step` método avanza el DVD-Video secuencia según el número de fotogramas especificado.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframes*
</dt> <dd>

Especifica el número de fotogramas que se pueden ir paso a paso como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, llame [**a CanStep**](canstep-method.md) para determinar si el descodificador admite la ejecución paso a paso de fotogramas.

Si el DVD-Video está reproduciendo en modo inverso cuando se llama a este método y el descodificador admite la ejecución paso a paso de fotograma inverso, la ejecución paso a paso del marco se realiza a la inversa.

 

 



