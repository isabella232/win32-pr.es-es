---
description: El método ShowCursor hace que el cursor sea visible cuando el objeto MSWebDVD está en modo de pantalla completa.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050525"
---
# <a name="showcursor-method"></a>ShowCursor (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowCursor` método hace que el cursor sea visible cuando el objeto **MSWebDVD** está en modo de pantalla completa.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Especifica si se debe mostrar el cursor como un valor booleano.



| Value | Descripción            |
|-------|------------------------|
| true  | Permite mostrar el cursor.        |
| false | No mostrar el cursor |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando la pantalla de DVD entra en modo de pantalla completa, el cursor desaparece en un plazo de entre 3 y 5 segundos. Use este método para que el cursor vuelva a estar visible si los botones de control de la aplicación están visibles en modo de pantalla completa.

 

 



