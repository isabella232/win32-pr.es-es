---
description: Agrega un objeto a la vista de Shell. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_ADDOBJECT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997812"
---
# <a name="sfvm_addobject-message"></a>SFVM \_ ADDOBJECT

Agrega un objeto a la vista de Shell. Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PIDL* \[ de\]
</dt> <dd>Puntero al objeto de interés que se va a agregar.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el nuevo identificador de elemento ListView del objeto agregado si el proceso se realizó correctamente; de lo contrario, devuelve-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




