---
description: El método GetGPRM recupera el registro de parámetros general especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: GetGPRM (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c46307f1cbec49b4916cdbd528c2b22cfb42bf89a06285c5c779339786599d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812565"
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

## <a name="remarks"></a>Comentarios

Este método no es necesario para ninguna funcionalidad de navegación o reproducción de DVD mediante **el objeto MSWebDVD.** Se proporciona para aquellos que tienen un conocimiento exhaustivo de la especificación de DVD que desean implementar características avanzadas. Los GPRM se pueden usar para contener cualquier valor, por lo que se pueden establecer y leer libremente. Sin embargo, dado que los GRM también se usan para almacenar comandos de disco, cambiar sus valores mediante [**SetGPRM**](setgprm-method.md) puede dar lugar a un comportamiento impredecible.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



