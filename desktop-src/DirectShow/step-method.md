---
description: El método Step avanza el flujo de DVD-Video por el número especificado de fotogramas.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Método Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678262"
---
# <a name="step-method"></a>Método Step

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Step` método avanza el flujo de DVD-Video por el número de fotogramas especificado.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Especifica el número de fotogramas que se van a recorrer como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame a [**CanStep**](canstep-method.md) para determinar si el descodificador admite la ejecución de fotogramas.

Si el DVD-Video se está reproduciendo en modo inverso cuando se llama a este método y el descodificador admite el recorrido de fotogramas inverso, el fotograma se ejecuta en orden inverso.

 

 



