---
description: Obtiene el nombre de la vista predeterminada. Llame a GetDisplayNameOf para recuperar los nombres de las otras vistas.
title: IShellFolderViewType::GetDefaultViewName (método)
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
ms.openlocfilehash: 252616bd2391606b9942777caf07a2f5f58627a316f51e481c19fbfcc98599b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443275"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType::GetDefaultViewName (método)

Obtiene el nombre de la vista predeterminada. Llame [**a GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar los nombres de las otras vistas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales; debe establecerse en 0.

</dd> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

Dirección de un puntero de cadena que recibe el nombre de vista predeterminado. La memoria de la cadena se asigna con [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




