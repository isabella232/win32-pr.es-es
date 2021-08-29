---
description: El método Add del objeto SWbemPropertySet agrega un objeto SWbemProperty a la colección SWbemPropertySet. Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza por la nueva definición.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Método SWbemPropertySet.Add (Wbemdisp.h)
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
ms.openlocfilehash: 52ee45eeb711254c18e8d81cd76fe598b0589fdb9d0e29b507e560fc3dccd167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897956"
---
# <a name="swbempropertysetadd-method"></a>Método SWbemPropertySet.Add

El **método Add** del objeto [**SWbemPropertySet**](swbempropertyset.md) agrega un objeto [**SWbemProperty**](swbemproperty.md) a la **colección SWbemPropertySet.** Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza por la nueva definición.

> [!Note]  
> El valor de la propiedad agregada es **NULL** (sin signo) después de esta operación. Para establecer o cambiar el valor de una propiedad WMI, debe establecer la propiedad [**Value**](swbemdatetime-value.md) del objeto [**SWbemProperty devuelto.**](swbemproperty.md)

 

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*strName* \[ En\]
</dt> <dd>

Obligatorio. Nombre de la nueva propiedad.

</dd> <dt>

*iCIMType* \[ En\]
</dt> <dd>

Obligatorio. Entero que representa el **calificador CIMType** de la nueva propiedad. Vea [**WbemCimTypeEnum para**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) obtener la lista con los calificadores **CIMType** y sus valores.

</dd> <dt>

*bIsArray* \[ in, opcional\]
</dt> <dd>

Especifica si la propiedad es un tipo de matriz. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado y debe ser cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve [**un objeto SWbemProperty**](swbemproperty.md) que representa la nueva propiedad. De lo contrario, **se devuelve** un objeto NULL.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Add,** el **objeto Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para que se ejecute este método.

</dd> <dt>

**wbemErrInvalidPropertyType** : 2147749930
</dt> <dd>

No se reconoce el calificador **CIMType.**

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de código que usa este método, vea el [**tema SWbemPropertySet.**](swbempropertyset.md)

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

[**SWbemPropertySet.Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty.Value**](swbemproperty-value.md)
</dt> </dl>

 

 




