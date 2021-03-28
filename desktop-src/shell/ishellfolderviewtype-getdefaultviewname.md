---
description: Obtiene el nombre de la vista predeterminada. Llame a GetDisplayNameOf para recuperar los nombres de las otras vistas.
title: 'IShellFolderViewType:: GetDefaultViewName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984630"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType:: GetDefaultViewName (método)

Obtiene el nombre de la vista predeterminada. Llame a [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar los nombres de las otras vistas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales; debe establecerse en 0.

</dd> <dt>

*ppwszName* \[ enuncia\]
</dt> <dd>

Tipo: **LPWStr \** _

Dirección de un puntero de cadena que recibe el nombre de vista predeterminado. La memoria de la cadena se asigna con [_ *SHStrDup* *](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




