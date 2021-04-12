---
description: El método Add del objeto SWbemQualifierSet agrega un objeto SWbemQualifier a la colección SWbemQualifierSet. Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361439"
---
# <a name="swbemqualifiersetadd-method"></a>SWbemQualifierSet. Add (método)

El método **Add** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) agrega un objeto [**SWbemQualifier**](swbemqualifier.md) a la colección **SWbemQualifierSet** . Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ de\]
</dt> <dd>

Obligatorio. Nombre del nuevo calificador.

</dd> <dt>

*varVal* \[ de\]
</dt> <dd>

Obligatorio. Valor de variante del nuevo calificador.

</dd> <dt>

*bPropagatesToSubclasses* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si este nuevo calificador se propaga a las subclases. El valor predeterminado es **true**.

</dd> <dt>

*bPropagatesToInstances* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si este nuevo calificador se propaga a las instancias de. El valor predeterminado es **true**.

</dd> <dt>

*bOverridable* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si se puede invalidar este calificador al propagarse. El valor predeterminado es **true**.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reservado. El valor predeterminado es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, este método devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) que representa el nuevo calificador. De lo contrario, se devuelve un objeto **null** .

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Add** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

El parámetro *iFlags* no era válido.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrCannotBeKey** -2147749919 (0x8004101F)
</dt> <dd>

Se produjo un intento no válido de especificar un calificador de **clave** en una propiedad que no puede ser una clave. Las claves se especifican en la definición de la clase de un objeto, y no se pueden modificar instancia por instancia.

</dd> <dt>

**wbemErrInvalidQualifierType** -2147749929 (0x80041029)
</dt> <dd>

El parámetro *varVal* no es de un tipo de calificador válido.

</dd> <dt>

**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)
</dt> <dd>

No es posible realizar la operación **SWbemQualifierSet. Add** en este calificador porque el objeto propietario no permite invalidaciones.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | \_ISWBEMQUALIFIERSET IID<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




