---
description: Quita un objeto de la vista de Shell. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_REMOVEOBJECT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986103"
---
# <a name="sfvm_removeobject-message"></a>SFVM \_ REMOVEOBJECT

Quita un objeto de la vista de Shell. Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PIDL* \[ de\]
</dt> <dd>PIDL del objeto que se va a quitar.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento que se quitó si se encontró un elemento que coincide con el PIDL especificado; de lo contrario, devuelve-1.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




