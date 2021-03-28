---
description: Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta de Shell.
title: 'IShellFolderSearchable:: InvalidateSearch (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275676"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>IShellFolderSearchable:: InvalidateSearch (método)

Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta de Shell.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidlSearch* \[ de\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Un puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la carpeta de búsqueda.

</dd> <dt>

*pdwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD \** _

Actualmente no hay marcas definidas; establézcalo en _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando se invalida una carpeta de búsqueda, puede realizar la limpieza de los recursos que ha usado. El método **IShellFolderSearchable:: InvalidateSearch** puede hacer que se cancele una búsqueda asincrónica y dará como resultado la versión final del objeto de interfaz [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




