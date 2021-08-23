---
description: Agrega un objeto a la vista Shell. Usado por el mensaje \_ SHShellFolderView.
title: SFVM_ADDOBJECT mensaje (Shlobj.h)
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
ms.openlocfilehash: 441ddac74e1640b2f836686c171d6fc896cbccee2dd6325c31041903ba610b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661065"
---
# <a name="sfvm_addobject-message"></a>Mensaje \_ ADDOBJECT de SFVM

Agrega un objeto a la vista Shell. Utilizado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidl* \[ En\]
</dt> <dd>Puntero al objeto de interés que se debe agregar.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el nuevo identificador de elemento listview del objeto agregado si el proceso se ha realizado correctamente; de lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




