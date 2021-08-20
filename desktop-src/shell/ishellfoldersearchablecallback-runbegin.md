---
description: Indica que se inició una búsqueda.
title: IShellFolderSearchableCallback::RunBegin (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 026b5b458736a0805d48dc59715a1705ecdb8557037232332767946dd05d333d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223355"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a>IShellFolderSearchableCallback::RunBegin (método)

Indica que se inició una búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwReserved* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

En respuesta a esta devolución de llamada, la aplicación puede habilitar el **botón Cancelar,** por ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




