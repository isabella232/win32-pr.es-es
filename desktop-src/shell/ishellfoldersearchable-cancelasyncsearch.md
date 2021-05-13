---
description: Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.
title: IShellFolderSearchable::CancelAsyncSearch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842996"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>IShellFolderSearchable::CancelAsyncSearch (método)

Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidlSearch* \[ En\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntero a [**itemidlist para**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) la búsqueda.

</dd> <dt>

*pdwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD \***

No hay marcas definidas actualmente; se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve S \_ OK si se cancela, o S FALSE \_ si la búsqueda no se está ejecutando.

## <a name="remarks"></a>Observaciones

Cuando la búsqueda se cancele realmente, se llamará a [**RunEnd.**](ishellfoldersearchablecallback-runend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




