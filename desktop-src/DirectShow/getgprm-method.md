---
description: El método GetGPRM recupera el registro de parámetros general especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: GetGPRM (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061125"
---
# <a name="getgprm-method"></a>GetGPRM (método)

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

Especifica el registro que se recuperará como entero. El valor debe oscilar entre 0 y 15.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el registro especificado.

## <a name="remarks"></a>Observaciones

Este método no es necesario para ninguna funcionalidad de navegación o reproducción de DVD mediante **el objeto MSWebDVD.** Se proporciona para aquellos que tienen un conocimiento exhaustivo de la especificación de DVD que desean implementar características avanzadas. Los GPRM se pueden usar para contener cualquier valor, por lo que se pueden establecer y leer libremente. Sin embargo, dado que los GPRM también se usan para almacenar comandos de disco, cambiar sus valores mediante [**SetGPRM**](setgprm-method.md) puede provocar un comportamiento imprevisible.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



