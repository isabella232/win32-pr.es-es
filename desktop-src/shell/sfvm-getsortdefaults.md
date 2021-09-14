---
description: Permite que el objeto de devolución de llamada especifique un parámetro de ordenación predeterminado. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_GETSORTDEFAULTS mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262500"
---
# <a name="sfvm_getsortdefaults-message"></a>Mensaje \_ DE SFVM GETSORTDEFAULTS

Permite que el objeto de devolución de llamada especifique un parámetro de ordenación predeterminado. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iDirection* \[ out\]
</dt> <dd>

Dirección de ordenación predeterminada. Establezca este parámetro en un valor positivo para ordenar en orden ascendente. Establezca este parámetro en cero o un valor negativo para ordenar en orden descendente.

</dd> <dt>

*iColumn* \[ out\]
</dt> <dd>

Columna usada para la ordenación. Esto se pasará a [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) en los 16 bits inferiores de su *valor lParam.*

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> : el objeto de vista de carpetas del sistema no reconoce **SFVM \_ GETSORTDEFAULTS.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
