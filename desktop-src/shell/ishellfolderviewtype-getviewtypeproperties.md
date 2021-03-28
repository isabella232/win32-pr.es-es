---
description: Obtiene las propiedades de la vista.
title: 'IShellFolderViewType:: GetViewTypeProperties (método)'
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
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984623"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>IShellFolderViewType:: GetViewTypeProperties (método)

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

*PIDL* \[ de\]
</dt> <dd>

Tipo: **PCUITEMID \_ secundario**

UN PIDL.

</dd> <dt>

*pdwFlags* \[ enuncia\]
</dt> <dd>

Tipo: **DWORD \** _

Puntero a una variable de entero sin signo que recibe las propiedades de la vista, que indican qué hacer cuando se selecciona la vista. Las marcas pueden ser cualquier combinación de los valores siguientes.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ Notify \_ Create** (0x00000001)


</dt> <dd>

Crear elemento de vista si no lo está.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFICAr a \_ Resort** (0x00000002)


</dt> <dd>

Vuelva a insertar PIDL y vuelva a ordenar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




