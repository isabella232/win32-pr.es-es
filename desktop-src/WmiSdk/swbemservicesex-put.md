---
description: Devuelve un objeto SWbemObjectPath que contiene la ruta de acceso del objeto en el que se escribieron los datos.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Método SWbemServicesEx.Put (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ee44d9341045e5adfc205b63dd8c6bb5a395994e6ff2bad1a7887e0a14823abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921373"
---
# <a name="swbemservicesexput-method"></a>Método SWbemServicesEx.Put

El **método Put** del objeto [**SWbemServicesEx**](swbemservicesex.md) guarda el objeto en el espacio de nombres enlazado al objeto y devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto en el que se escribieron los datos.

Se llama a este método en el modo semisincronoso. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Obligatorio. Nuevo objeto que se va a colocar en el espacio de nombres . Puede ser un objeto recién creado o un objeto modificado.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Este parámetro determina si la llamada crea o actualiza el objeto y si la llamada se devuelve inmediatamente. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))


</dt> <dd>

Permite actualizar una clase si no hay clases derivadas y no hay instancias para esa clase. También permite actualizaciones en todos los casos si el cambio es solo para calificadores no importantes (por ejemplo, el **calificador Description).** Este es el comportamiento predeterminado de esta llamada y se usa para la compatibilidad con versiones anteriores de WMI. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))


</dt> <dd>

Permite actualizaciones de clases incluso si hay clases secundarias, cuando el cambio no provoca ningún conflicto con las clases secundarias. Puede usar esta marca al agregar una nueva propiedad a una clase base que no se mencionó anteriormente en ninguna de las clases secundarias. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))


</dt> <dd>

Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto. Por ejemplo, esta marca fuerza una actualización si se definió un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador en conflicto con el existente. En el modo force, este conflicto se resuelve mediante la eliminación del calificador en conflicto en la clase secundaria. Si la clase tiene instancias, se produce un error en la actualización.

El uso del modo force para actualizar una clase estática provoca la eliminación de todas las instancias de esa clase. Una actualización forzada en una clase de proveedor no elimina instancias de la clase .

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))


</dt> <dd>

Hace que la clase o instancia se cree si no existe o se sobrescriba si ya existe.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))


</dt> <dd>

Solo se usa para la creación. Se produce un error en la llamada si la clase o instancia ya existe.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))


</dt> <dd>

Hace que esta llamada solo realice una actualización. La clase o instancia debe existir para que la llamada sea correcta.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Hace que esta llamada se bloquee hasta que se haya completado la operación. Esta marca llama al método en modo sincrónico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI escriba datos de modificación de clase, así como la definición de clase base. Para obtener más información, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que proporciona servicios a la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectPath.**](swbemobjectpath.md) Este objeto contiene la ruta de acceso del objeto de la instancia o clase que se ha confirmado correctamente en WMI.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Put,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene el permiso para la operación.

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

Se **especificó un valor NULL** para una propiedad que no puede ser **NULL.** Un ejemplo de este tipo de propiedad es uno marcado por un calificador [**Key**](standard-qualifiers.md), **Indexed** o **Not \_ Null.**

</dd> <dt>

**wbemErrInvalidObject:** 2147749908 (0x80041014)
</dt> <dd>

El objeto especificado no es válido.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
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
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



 

 




