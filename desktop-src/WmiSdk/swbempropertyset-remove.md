---
description: El método Remove del objeto SWbemPropertySet elimina una propiedad de la colección SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155825"
---
# <a name="swbempropertysetremove-method"></a>SWbemPropertySet. Remove (método)

El método **Remove** del objeto [**SWbemPropertySet**](swbempropertyset.md) elimina una propiedad de la colección **SWbemPropertySet** .

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ de\]
</dt> <dd>

Obligatorio. Nombre del elemento que se va a quitar.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reservado. Este valor debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

El usuario intentó eliminar una propiedad que no se puede eliminar.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

La propiedad especificada no existe.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para que se ejecute este método.

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380)
</dt> <dd>

El usuario intentó eliminar una propiedad que no era propiedad. Se trataba de una propiedad heredada de una clase principal.

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002)
</dt> <dd>

El usuario eliminó un valor predeterminado de invalidación para la clase actual. Se ha reactivado el valor predeterminado de esta propiedad en la clase primaria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las propiedades no se pueden quitar de las instancias de clase ni de las clases derivadas con propiedades heredadas. Estos intentos de eliminación provocan un error y no se quita la propiedad. la propiedad se restablece a su valor predeterminado.

No se puede recorrer en iteración una colección mientras se quitan elementos porque cuando se quita un elemento de una colección, el puntero de la colección se mueve al siguiente elemento. Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de código que usa este método, vea el tema [**SWbemPropertySet**](swbempropertyset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | \_ISWBEMPROPERTYSET IID<br/>                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




