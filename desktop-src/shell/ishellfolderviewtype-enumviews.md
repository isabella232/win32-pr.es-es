---
description: Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista extendida.
title: IShellFolderViewType::EnumViews (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 203ee36994ca3a622d564f637598f4ef22b8494200e5d57faa1d47cb290fd49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220341"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>IShellFolderViewType::EnumViews (método)

Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista extendida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*grfFlags* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Marcas que indican qué elementos se incluirán en la enumeración . Para obtener una lista de los valores posibles, vea el tipo enumerado [**SHCONTF.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) Este parámetro se puede omitir.

</dd> <dt>

*mio* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Dirección de una variable de puntero de tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) que recibe el enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Las vistas se representan al usuario como carpetas ocultas fuera del directorio raíz (representado por PIDL). Siempre que sea necesario, la vista predeterminada (fuera de la carpeta raíz) se representa como **EL PIDL** NULL o vacío.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




