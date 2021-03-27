---
description: Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista ampliada.
title: 'IShellFolderViewType:: EnumViews (método)'
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
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997280"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>IShellFolderViewType:: EnumViews (método)

Recupera un enumerador que devolverá un puntero a una lista de identificadores de elemento (PIDL) para cada vista ampliada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*grfFlags* \[ de\]
</dt> <dd>

Tipo: **ULong**

Marcas que indican qué elementos se van a incluir en la enumeración. Para obtener una lista de los valores posibles, vea el tipo enumerado [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) . Este parámetro se puede omitir.

</dd> <dt>

*ppenum* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Dirección de una variable de puntero de tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) que recibe el enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las vistas se representan al usuario como carpetas ocultas fuera del directorio raíz (representado por PIDL). Siempre que sea necesario, la vista predeterminada (fuera de la carpeta raíz) se representa como **null**, o está vacía, PIDL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




