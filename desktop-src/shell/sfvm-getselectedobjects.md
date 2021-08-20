---
description: Recupera una matriz de punteros a listas de identificadores de elemento (PIDL) para todos los objetos seleccionados. Lo usa shshellfolderview \_ message.
title: SFVM_GETSELECTEDOBJECTS mensaje (Shlobj.h)
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
ms.openlocfilehash: 7e892755b3c9bec0d955ddc786b818eac8d04e865acb710d1d5064c7f4102e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677232"
---
# <a name="sfvm_getselectedobjects-message"></a>Mensaje \_ DE SFVM GETSELECTEDOBJECTS

Recupera una matriz de punteros a listas de identificadores de elemento (PIDL) para todos los objetos seleccionados. Usado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pppdl* \[ out\]
</dt> <dd>Dirección de una matriz de PIDL de objetos seleccionados actualmente.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos de la matriz.

## <a name="remarks"></a>Comentarios

Cuando termine, debe llamar a [**ILFree en**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) cada miembro de la matriz para liberar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




