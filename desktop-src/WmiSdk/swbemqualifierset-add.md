---
description: El método Add del objeto SWbemQualifierSet agrega un objeto SWbemQualifier a la colección SWbemQualifierSet. Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet.Add (Wbemdisp.h)
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
ms.openlocfilehash: 64a85e10614595d9dd6492d3f4b412f1d89432c0188801ea60a09e294846297b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897785"
---
# <a name="swbemqualifiersetadd-method"></a>Método SWbemQualifierSet.Add

El **método Add** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) agrega un objeto [**SWbemQualifier**](swbemqualifier.md) a la **colección SWbemQualifierSet.** Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*strName* \[ En\]
</dt> <dd>

Obligatorio. Nombre del nuevo calificador.

</dd> <dt>

*varVal* \[ En\]
</dt> <dd>

Obligatorio. Valor variant del nuevo calificador.

</dd> <dt>

*bPropsubclassesToSubclasses* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si este nuevo calificador se propaga a subclases. El valor predeterminado es **TRUE.**

</dd> <dt>

*bPropinstancesToInstances* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si este nuevo calificador se propaga a instancias de . El valor predeterminado es **TRUE.**

</dd> <dt>

*bOverríble* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si este calificador se puede invalidar cuando se propaga. El valor predeterminado es **TRUE.**

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. El valor predeterminado es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve [**un objeto SWbemQualifier**](swbemqualifier.md) que representa el nuevo calificador. De lo contrario, **se devuelve** un objeto NULL.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Add,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

El *parámetro iFlags* no era válido.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrCannotBeKey:** 2147749919 (0x8004101F)
</dt> <dd>

Hubo un intento no válido de especificar un **calificador de** clave en una propiedad que no puede ser una clave. Las claves se especifican en la definición de la clase de un objeto, y no se pueden modificar instancia por instancia.

</dd> <dt>

**wbemErrInvalidQualifierType:** 2147749929 (0x80041029)
</dt> <dd>

El *parámetro varVal* no es de un tipo de calificador legal.

</dd> <dt>

**wbemErrOverrideNotAllowed:** 2147749914 (0x8004101A)
</dt> <dd>

No es posible realizar la operación **SWbemQualifierSet.Add** en este calificador porque el objeto propietario no permite invalidaciones.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




