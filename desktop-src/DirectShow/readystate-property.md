---
description: La propiedad ReadyState recupera el ReadyState del objeto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propiedad ReadyState (Ocidl. h)
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
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679438"
---
# <a name="readystate-property"></a>Propiedad ReadyState

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `ReadyState` propiedad recupera el ReadyState del objeto **MSWebDVD** .

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el objeto ReadyState del control.



| Código devuelto | Descripción                                               |
|-------------|-----------------------------------------------------------|
| 0           | Estado de inicialización predeterminado.                             |
| 1           | El objeto está cargando sus propiedades.                         |
| 2           | El objeto se ha inicializado.                              |
| 3           | El objeto es interactivo, pero no todos sus datos están disponibles. |
| 4           | El objeto ha recibido todos sus datos.                         |



 

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.

Cualquier objeto incrustado en una página web expone la `ReadyState` propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



 

 




