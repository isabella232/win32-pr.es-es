---
description: El método DVDAdm.GetParentalLevel recupera el nivel parental que se guardó por última vez en el registro.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: GetParentalLevel (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d188dbc38e89d49291623c99333fdd05372c26d8fcd5da728dcad5393761e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756665"
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

## <a name="remarks"></a>Comentarios

El nivel parental que recupera este método no es necesariamente el mismo nivel almacenado actualmente en el control MSWebDVD; Para obtener el nivel almacenado actualmente en el control , llame al [**método GetPlayerParentalLevel.**](getplayerparentallevel-method.md) Un valor de -1 indica que la administración parental está deshabilitada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



