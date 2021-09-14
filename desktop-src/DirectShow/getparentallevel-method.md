---
description: El método DVDAdm.GetParentalLevel recupera el nivel parental que se guardó por última vez en el registro.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: GetParentalLevel (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061118"
---
# <a name="getparentallevel-method"></a>GetParentalLevel (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.GetParentalLevel` método recupera el nivel parental que se guardó por última vez en el registro.

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un entero del 1 al 8 que indica el nivel parental predeterminado.

## <a name="remarks"></a>Observaciones

El nivel parental que recupera este método no es necesariamente el mismo nivel almacenado actualmente en el control MSWebDVD; Para obtener el nivel almacenado actualmente en el control , llame al [**método GetPlayerParentalLevel.**](getplayerparentallevel-method.md) Un valor de -1 indica que la administración parental está deshabilitada.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



