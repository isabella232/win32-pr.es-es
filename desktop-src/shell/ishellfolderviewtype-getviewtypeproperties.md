---
description: Obtiene las propiedades de la vista.
title: IShellFolderViewType::GetViewTypeProperties (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: 57e053321bbd17c90fbe82832cdb01e9acb6994438d22cb72ef62bf1e7143dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220313"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>IShellFolderViewType::GetViewTypeProperties (método)

Obtiene las propiedades de la vista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidl* \[ En\]
</dt> <dd>

Tipo: **PCUITEMID \_ CHILD**

A PIDL.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Tipo: **DWORD \***

Puntero a una variable de entero sin signo que recibe las propiedades de vista, que indican qué hacer cuando se selecciona la vista. Las marcas pueden ser cualquier combinación de los valores siguientes.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)


</dt> <dd>

Cree un elemento de vista si no está ahí.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)


</dt> <dd>

Vuelva a insertar PIDL y vuelva a ordenar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




