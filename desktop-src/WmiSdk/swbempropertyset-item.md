---
description: El método Item del objeto SWbemPropertySet obtiene una propiedad denominada SWbemProperty de la colección. Este es el método predeterminado para este objeto .
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Método SWbemPropertySet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567225"
---
# <a name="swbempropertysetitem-method"></a>Método SWbemPropertySet.Item

El **método Item** del objeto [**SWbemPropertySet**](swbempropertyset.md) obtiene una propiedad denominada [**SWbemProperty**](swbemproperty.md) de la colección. Este es el método predeterminado para este objeto .

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ En\]
</dt> <dd>

Necesario. Nombre de la propiedad que se recuperará.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. Este valor debe ser cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, se devuelve el objeto [**SWbemProperty**](swbemproperty.md) solicitado.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Item,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749896
</dt> <dd>

No hay suficiente memoria para que se ejecute este método.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



 

 




