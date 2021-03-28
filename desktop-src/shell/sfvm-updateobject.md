---
description: Actualiza un objeto pasando un puntero a una matriz de dos punteros a listas de identificadores de elemento (PIDL). Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_UPDATEOBJECT (ShlObj. h)
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
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279387"
---
# <a name="sfvm_updateobject-message"></a>SFVM \_ UPDATEOBJECT

Actualiza un objeto pasando un puntero a una matriz de dos punteros a listas de identificadores de elemento (PIDL). Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppidl* \[ de\]
</dt> <dd>

Dirección de una matriz de dos PIDL. El primer PIDL es el PIDL antiguo. La segunda es una copia del antiguo PIDL con información actualizada. El control sobre la duración de la copia pertenece a la vista después de la finalización correcta de esta llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ID. de ListView del objeto actualizado si la actualización se realizó correctamente; de lo contrario, devuelve-1.

## <a name="remarks"></a>Observaciones

Si la actualización no se realizó correctamente, el llamador debe liberar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




