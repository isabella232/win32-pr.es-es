---
description: El método Remove del objeto SWbemPropertySet elimina una propiedad de la colección SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Método SWbemPropertySet.Remove (Wbemdisp.h)
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
ms.openlocfilehash: 7a79c99243cbbb18e761295980b98e56a6db926e3885de6ed2d0b53aafe084db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897915"
---
# <a name="swbempropertysetremove-method"></a>Método SWbemPropertySet.Remove

El **método Remove** del objeto [**SWbemPropertySet**](swbempropertyset.md) elimina una propiedad de la **colección SWbemPropertySet.**

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ En\]
</dt> <dd>

Obligatorio. Nombre del elemento que se quitará.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reservado. Este valor debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Remove,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidOperation:** 2147749910 (0x80041016)
</dt> <dd>

El usuario intentó eliminar una propiedad que no se puede eliminar.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

La propiedad especificada no existe.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para que se ejecute este método.

</dd> <dt>

**wbemErrProppropproperty:** 142927303552 (0x2147219380)
</dt> <dd>

El usuario intentó eliminar una propiedad que no era propiedad de . Se trataba de una propiedad heredada de una clase principal.

</dd> <dt>

**wbemErrResetToDefault:** 2147758082 (0x80043002)
</dt> <dd>

El usuario eliminó un valor predeterminado de invalidación para la clase actual. Se ha reactivado el valor predeterminado de esta propiedad en la clase primaria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las propiedades no se pueden quitar de instancias de clase ni clases derivadas con propiedades heredadas. Estos intentos de eliminación genera un error y la propiedad no se quita; la propiedad se restablece a su valor predeterminado.

No se puede iterar una colección al quitar elementos porque cuando se quita un elemento de una colección, el puntero de colección se mueve al elemento siguiente. Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de código que use este método, vea el [**tema SWbemPropertySet.**](swbempropertyset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet.Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




