---
description: Inicia una búsqueda de una cadena de búsqueda especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable:: FindString (método) (MMC. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810946"
---
# <a name="ishellfoldersearchablefindstring-method"></a>IShellFolderSearchable:: FindString (método)

Inicia una búsqueda de una cadena de búsqueda especificada.

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

*pwszTarget* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica la palabra clave de búsqueda.

</dd> <dt>

*pdwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD \** _

Actualmente no hay marcas definidas; establézcalo en _ * NULL * *.

</dd> <dt>

*punkOnAsyncSearch* \[ de\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Un puntero a un objeto de tipo [_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown). Este objeto debe admitir la interfaz [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) . Se establece en **null** si no se necesita ninguna devolución de llamada.

</dd> <dt>

*ppidlOut* \[ enuncia\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Puntero a una estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la carpeta de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
