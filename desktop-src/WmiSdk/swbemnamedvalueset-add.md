---
description: El método Add del objeto SWbemNamedValueSet agrega un objeto SWbemNamedValue a la colección. Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544667"
---
# <a name="swbemnamedvaluesetadd-method"></a>SWbemNamedValueSet. Add (método)

El método **Add** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) agrega un objeto [**SWbemNamedValue**](swbemnamedvalue.md) a la colección. Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ de\]
</dt> <dd>

Obligatorio. Nombre del nuevo valor.

</dd> <dt>

*varVal* \[ de\]
</dt> <dd>

Obligatorio. Variante que representa el nuevo valor.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reserved y debe establecerse en cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, este método devuelve el objeto [**SWbemNamedValue**](swbemnamedvalue.md) recién modificado o recién creado.

## <a name="remarks"></a>Observaciones

Para obtener ejemplos de cómo agregar y recuperar valores con nombre, vea [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | \_ISWBEMNAMEDVALUESET IID<br/>                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




