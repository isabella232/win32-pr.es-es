---
description: Recupera una matriz de punteros a listas de identificadores de elementos (PIDL) para todos los objetos seleccionados. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_GETSELECTEDOBJECTS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913314"
---
# <a name="sfvm_getselectedobjects-message"></a>SFVM \_ GETSELECTEDOBJECTS

Recupera una matriz de punteros a listas de identificadores de elementos (PIDL) para todos los objetos seleccionados. Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppidl* \[ enuncia\]
</dt> <dd>Dirección de una matriz de PIDL de los objetos seleccionados actualmente.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos de la matriz.

## <a name="remarks"></a>Observaciones

Cuando termine, debe llamar a [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) en cada miembro de la matriz para liberar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




