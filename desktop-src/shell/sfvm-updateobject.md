---
description: Actualiza un objeto pasando un puntero a una matriz de dos punteros a listas de identificadores de elemento (PIDL). Usado por el mensaje \_ SHShellFolderView.
title: SFVM_UPDATEOBJECT mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452857"
---
# <a name="sfvm_updateobject-message"></a>Mensaje \_ UPDATEOBJECT de SFVM

Actualiza un objeto pasando un puntero a una matriz de dos punteros a listas de identificadores de elemento (PIDL). Utilizado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pppdl* \[ En\]
</dt> <dd>

Dirección de una matriz de dos PIDL. El primer PIDL es el PIDL antiguo. La segunda es una copia del PIDL anterior con información actualizada. El control sobre la duración de la copia pertenece a la vista después de completar correctamente esta llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de listview del objeto actualizado si la actualización se ha realizado correctamente; de lo contrario, devuelve -1.

## <a name="remarks"></a>Observaciones

Si la actualización no se ha actualizado correctamente, el autor de la llamada debe liberar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




