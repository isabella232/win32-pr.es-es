---
description: El método GetGPRM recupera el registro de parámetros general especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Método GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537887"
---
# <a name="getgprm-method"></a>Método GetGPRM

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetGPRM` método recupera el registro de parámetros general especificado.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica el registro que se va a recuperar como un entero. El valor debe oscilar entre 0 y 15.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el registro especificado.

## <a name="remarks"></a>Observaciones

Este método no es necesario para ninguna funcionalidad de navegación o reproducción de DVD que use el objeto **MSWebDVD** . Se proporciona a los usuarios con un conocimiento exhaustivo de la especificación de DVD que desea implementar características avanzadas. GPRMs se puede usar para contener cualquier valor, por lo que se pueden establecer y leer libremente. Pero como GPRMs se usan también para almacenar comandos de disco, el cambio de sus valores con [**SetGPRM**](setgprm-method.md) puede producir un comportamiento impredecible.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



