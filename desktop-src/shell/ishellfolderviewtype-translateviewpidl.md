---
description: Reconstruye un puntero a una lista de identificadores de elemento (PIDL) a partir de una representación jerárquica de la carpeta de Shell en una representación diferente.
title: 'IShellFolderViewType:: TranslateViewPidl (método)'
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
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543107"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>IShellFolderViewType:: TranslateViewPidl (método)

Reconstruye un puntero a una lista de identificadores de elemento (PIDL) a partir de una representación jerárquica de la carpeta de Shell en una representación diferente.

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

*PIDL* \[ de\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

La matriz de identificadores de elemento relativa a la carpeta raíz.

</dd> <dt>

*pidlView* \[ de\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

PIDL especial de la vista.

</dd> <dt>

*ppidlOut* \[ de\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relative \** _

La dirección de una variable PIDL para recibir la traducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando termine, debe liberar el PIDL devuelto con [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




