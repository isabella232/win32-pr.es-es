---
description: La propiedad ReadyState recupera readyState del objeto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propiedad ReadyState (Ocidl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: 029798e66d8ed69dc18bbb23dafc8b047d770f1bc91ac1b86ca7bdb09963c2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072789"
---
# <a name="readystate-property"></a>Propiedad ReadyState

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `ReadyState` propiedad recupera el valor ReadyState del objeto **MSWebDVD.**

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa readyState del control.



| Código devuelto | Descripción                                               |
|-------------|-----------------------------------------------------------|
| 0           | Estado de inicialización predeterminado.                             |
| 1           | El objeto está cargando sus propiedades.                         |
| 2           | Se ha inicializado el objeto .                              |
| 3           | El objeto es interactivo, pero no todos sus datos están disponibles. |
| 4           | El objeto ha recibido todos sus datos.                         |



 

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado.

Cualquier objeto incrustado en una página web expone la `ReadyState` propiedad .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



 

 




