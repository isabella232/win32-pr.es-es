---
description: El método ShowCursor hace que el cursor esté visible cuando el objeto MSWebDVD está en modo de pantalla completa.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Método ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906665"
---
# <a name="showcursor-method"></a>Método ShowCursor

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowCursor` método hace que el cursor esté visible cuando el objeto **MSWebDVD** está en modo de pantalla completa.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Especifica si se va a mostrar el cursor como booleano.



| Value | Descripción            |
|-------|------------------------|
| true  | Permite mostrar el cursor.        |
| false | No mostrar el cursor |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando la pantalla del DVD entra en el modo de pantalla completa, el cursor desaparece entre 3 y 5 segundos. Use este método para hacer que el cursor sea visible de nuevo si los botones de control de la aplicación están visibles en el modo de pantalla completa.

 

 



