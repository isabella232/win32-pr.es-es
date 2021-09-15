---
description: Reconstruye un puntero a una lista de identificadores de elemento (PIDL) de una representación jerárquica de la carpeta Shell en una representación diferente.
title: IShellFolderViewType::TranslateViewPidl (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468136"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>IShellFolderViewType::TranslateViewPidl (método)

Reconstruye un puntero a una lista de identificadores de elemento (PIDL) de una representación jerárquica de la carpeta Shell en una representación diferente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidl* \[ En\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE**

Matriz de los IDs de elemento relativos a la carpeta raíz.

</dd> <dt>

*pidlView* \[ En\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE**

PIDL especial de la vista.

</dd> <dt>

*pppdlOut* \[ En\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE \***

Dirección de una variable PIDL para recibir la traducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Cuando termine, debe liberar el PIDL devuelto con [**ILFree.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




