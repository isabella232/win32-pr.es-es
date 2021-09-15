---
description: Comienza una búsqueda de una cadena de búsqueda especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: Método IShellFolderSearchable::FindString (Mmc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468152"
---
# <a name="ishellfoldersearchablefindstring-method"></a>IShellFolderSearchable::FindString (método)

Comienza una búsqueda de una cadena de búsqueda especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszTarget* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica la palabra clave search.

</dd> <dt>

*pdwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD \***

No hay marcas definidas actualmente; se establece en **NULL.**

</dd> <dt>

*yonAsyncSearch* \[ En\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero a un objeto de tipo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Este objeto debe admitir la [**interfaz IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md) Establezca en **NULL si** no es necesaria ninguna devolución de llamada.

</dd> <dt>

*pppdlOut* \[ out\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Puntero a una estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la carpeta de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Mmc.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
