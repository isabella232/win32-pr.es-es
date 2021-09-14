---
description: El método Add del objeto SWbemNamedValueSet agrega un objeto SWbemNamedValue a la colección. Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet.Add (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967099"
---
# <a name="swbemnamedvaluesetadd-method"></a>Método SWbemNamedValueSet.Add

El **método Add** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) agrega un objeto [**SWbemNamedValue**](swbemnamedvalue.md) a la colección. Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*strName* \[ En\]
</dt> <dd>

Necesario. Nombre del nuevo valor.

</dd> <dt>

*varVal* \[ En\]
</dt> <dd>

Necesario. Variante que representa el nuevo valor.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reservado y deben establecerse en cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve el objeto [**SWbemNamedValue**](swbemnamedvalue.md) recién modificado o recién creado.

## <a name="remarks"></a>Observaciones

Para obtener ejemplos de cómo agregar y recuperar valores con nombre, vea [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




