---
description: El método CanStep determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución paso a paso del marco en una dirección especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: CanStep (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160233"
---
# <a name="canstep-method"></a>CanStep (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `CanStep` método determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución paso a paso del marco en una dirección especificada.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Booleano que se usa como marca para especificar la dirección, hacia delante o hacia atrás, de la capacidad de paso a paso del marco del descodificador.



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | ¿Puede el descodificador retroceder?                           |
| false | ¿Puede el descodificador avanzar? Este es el valor predeterminado. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano de true si el descodificador puede ir en la dirección especificada y false en caso contrario.

## <a name="remarks"></a>Observaciones

No todos los descodificadores MPEG-2 de hardware admiten las nuevas funcionalidades de ejecución paso a paso de fotogramas DirectShow® 8.0. Este método consulta al descodificador sus funcionalidades de ejecución paso a paso por fotogramas. Si el descodificador puede realizar la ejecución paso a paso de fotogramas, una aplicación puede usar el [**método Step**](step-method.md) para pasar por los fotogramas. Este método siempre devolverá **true si** se usa un descodificador de software.

 

 



