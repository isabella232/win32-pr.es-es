---
description: El método Add del objeto SWbemPropertySet agrega un objeto SWbemProperty a la colección SWbemPropertySet. Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza con la nueva definición.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716989"
---
# <a name="swbempropertysetadd-method"></a>SWbemPropertySet. Add (método)

El método **Add** del objeto [**SWbemPropertySet**](swbempropertyset.md) agrega un objeto [**SWbemProperty**](swbemproperty.md) a la colección **SWbemPropertySet** . Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza con la nueva definición.

> [!Note]  
> El valor de la propiedad agregada es **null** (sin asignar) después de esta operación. Para establecer o cambiar el valor de una propiedad de WMI, debe establecer la propiedad [**Value**](swbemdatetime-value.md) del objeto [**SWbemProperty**](swbemproperty.md) devuelto.

 

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ de\]
</dt> <dd>

Obligatorio. Nombre de la nueva propiedad.

</dd> <dt>

*iCIMType* \[ de\]
</dt> <dd>

Obligatorio. Entero que representa el calificador **CIMType** de la nueva propiedad. Vea [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) para obtener la lista con los calificadores **CIMType** y sus valores.

</dd> <dt>

*bIsArray* \[ en, opcional\]
</dt> <dd>

Especifica si la propiedad es un tipo de matriz. El valor predeterminado de este parámetro es **false**.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reserved y debe ser cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, este método devuelve un objeto [**SWbemProperty**](swbemproperty.md) que representa la nueva propiedad. De lo contrario, se devuelve un objeto **null** .

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Add** , el objeto **Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para que se ejecute este método.

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

No se reconoce el calificador **CIMType** .

</dd> </dl>

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

[**SWbemPropertySet. Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




