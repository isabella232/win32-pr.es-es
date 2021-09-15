---
description: Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta Shell.
title: IShellFolderSearchable::InvalidateSearch (método)
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
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468151"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>IShellFolderSearchable::InvalidateSearch (método)

Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta Shell.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidlSearch* \[ En\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) de la carpeta de búsqueda.

</dd> <dt>

*pdwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD \***

No hay marcas definidas actualmente; se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Cuando se invalida una carpeta de búsqueda, puede realizar la limpieza de los recursos que ha usado. El **método IShellFolderSearchable::InvalidateSearch** puede hacer que se cancele una búsqueda asincrónica y dará lugar a la versión final del objeto de interfaz [**IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




