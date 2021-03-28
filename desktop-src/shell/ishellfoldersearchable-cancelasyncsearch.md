---
description: Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.
title: 'IShellFolderSearchable:: CancelAsyncSearch (método)'
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
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984638"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>IShellFolderSearchable:: CancelAsyncSearch (método)

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

*pidlSearch* \[ de\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Un puntero a un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la búsqueda.

</dd> <dt>

*pdwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD \** _

Actualmente no hay marcas definidas; establézcalo en _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve S \_ OK si se cancela o s \_ false si la búsqueda no se está ejecutando.

## <a name="remarks"></a>Observaciones

Cuando la búsqueda se cancela realmente, se llamará a [**RunEnd**](ishellfoldersearchablecallback-runend.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




