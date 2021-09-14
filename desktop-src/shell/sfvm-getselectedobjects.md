---
description: Recupera una matriz de punteros a listas de identificadores de elemento (PIDL) para todos los objetos seleccionados. Usado por el mensaje \_ SHShellFolderView.
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
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262511"
---
# <a name="sfvm_getselectedobjects-message"></a>Mensaje \_ DE SFVM GETSELECTEDOBJECTS

Recupera una matriz de punteros a listas de identificadores de elemento (PIDL) para todos los objetos seleccionados. Utilizado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


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

## <a name="remarks"></a>Observaciones

Cuando termine, debe llamar a [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) en cada miembro de la matriz para liberar la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




