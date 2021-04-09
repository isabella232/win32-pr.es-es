---
description: El método CanStep determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución de fotogramas en una dirección especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Método CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079921"
---
# <a name="canstep-method"></a>Método CanStep

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `CanStep` método determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución paso a paso en una dirección especificada.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Valor booleano que se usa como marcador para especificar la dirección, hacia delante o hacia atrás, de la capacidad de recorrido de fotogramas del descodificador.



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | ¿Se puede descodificar el paso atrás?                           |
| false | ¿El paso del descodificador puede avanzar? Este es el valor predeterminado. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano true si el descodificador puede entrar en la dirección especificada y false en caso contrario.

## <a name="remarks"></a>Observaciones

No todos los descodificadores MPEG-2 de hardware admiten las nuevas capacidades de recorrido de fotogramas en DirectShow® 8,0. Este método consulta el descodificador para obtener la funcionalidad de ejecución de fotogramas. Si el descodificador puede realizar la ejecución paso a paso, una aplicación puede utilizar el método [**Step**](step-method.md) para recorrer los fotogramas. Este método siempre devolverá **true** si se usa un descodificador de software.

 

 



