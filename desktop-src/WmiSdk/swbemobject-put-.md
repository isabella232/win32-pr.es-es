---
description: El método Put de SWbemObject crea o actualiza una instancia o un objeto de clase \_ para Windows Management Instrumentation (WMI). Puede usar este método después de modificar las propiedades o métodos de un objeto SWbemObject, y los cambios se escriben en WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9310f690ea9ffc153e88ee9b0cd5ed489beef107c048f7e00e6891a69800b957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991975"
---
# <a name="swbemobjectput_-method"></a>Método SWbemObject.Put \_

El **\_ método Put** de [**SWbemObject**](swbemobject.md) crea o actualiza una instancia o un objeto de clase para Windows Management Instrumentation (WMI). Puede usar este método después de modificar las propiedades o métodos de **un objeto SWbemObject** y los cambios se escriben en WMI.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Este parámetro determina si la llamada crea o actualiza la clase o instancia y si la llamada se devuelve inmediatamente. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible** (0 (0x0))


</dt> <dd>

Permite actualizar una clase si no hay clases derivadas y no hay instancias para esa clase. También permite actualizaciones en todos los casos si el cambio es simplemente para calificadores no importantes (por ejemplo, el **calificador Description).** Este es el comportamiento predeterminado de esta llamada y se usa para la compatibilidad con versiones anteriores de WMI. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode** (32 (0x20))


</dt> <dd>

Permite actualizaciones de clases incluso si hay clases secundarias si el cambio no provoca ningún conflicto con las clases secundarias. Puede usar esta marca al agregar una nueva propiedad a una clase base que no se mencionó anteriormente en ninguna de las clases secundarias. Si la clase tiene instancias, se produce un error en la actualización. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode** (64 (0x40))


</dt> <dd>

Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto. Por ejemplo, esta marca forzará una actualización si se definió un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador y entra en conflicto con el existente. En modo de fuerza, este conflicto se resolvería eliminando el calificador en conflicto en la clase secundaria. Si la clase tiene instancias, se producirá un error en la actualización.

El uso del modo force para actualizar una clase estática da lugar a la eliminación de todas las instancias de esa clase. Una actualización forzada en una clase de proveedor no elimina instancias de la clase .

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate** (0 (0x0))


</dt> <dd>

Hace que la clase o instancia se cree si no existe o se sobrescribe si ya existe.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly** (2 (0x2))


</dt> <dd>

Solo se usa para la creación. Se produce un error en la llamada si la clase o instancia ya existe.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly** (1 (0x1))


</dt> <dd>

Hace que esta llamada se actualice. La clase o instancia debe existir para que la llamada sea correcta.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Hace que esta llamada se bloquee hasta que se haya completado la consulta.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI escriba datos de modificación de clase, así como la definición de clase base. Para obtener más información sobre los calificadores modificados, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un [**objeto SWbemObjectPath**](swbemobjectpath.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectPath.**](swbemobjectpath.md) Este objeto contiene la ruta de acceso del objeto de la instancia o clase que se ha confirmado correctamente en WMI.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ Put,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied** : 2147749891
</dt> <dd>

El usuario actual no tiene permiso para actualizar una instancia de la clase especificada.

</dd> <dt>

**wbemErrAlreadyExists:** 2147749913 (0x80041019)
</dt> <dd>

Se especificó la marca **wbemChangeFlagCreateOnly,** pero la instancia ya existe.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrGalegalNull:** 2147749898 (0x8004100A)
</dt> <dd>

Se especificó **un valor de Nothing** para una propiedad que puede no ser **Nothing.** Un ejemplo de esta propiedad es uno marcado por un calificador **Key,** **Indexed** o **Not \_ Null.**

</dd> <dt>

**wbemErrInvalidObject:** 2147749908 (0x80041014)
</dt> <dd>

La instancia especificada no es válida.

</dd> <dt>

**wbemErrInvalidParameter** : 0x80041008
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrNotFound** : 2147749890 (0x80041002)
</dt> <dd>

Se especificó la marca **wbemChangeFlagUpdateOnly,** pero la instancia o clase no existe.

</dd> <dt>

**wbemErrIncompleteClass** : 2147749920 (0x80041020)
</dt> <dd>

No se han establecido todas las propiedades necesarias para las clases.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObjectPath.Class**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

