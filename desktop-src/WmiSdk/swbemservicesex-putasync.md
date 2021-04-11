---
description: Guarda un objeto de forma asincrónica en un espacio de nombres. Cuando se realiza correctamente, este método envía un evento alcompleto al objeto SWbemSink que se especifica como parámetro de entrada.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Método SWbemServicesEx. PutAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082974"
---
# <a name="swbemservicesexputasync-method"></a>SWbemServicesEx. PutAsync, método

El método **PutAsync** del objeto [**SWbemServicesEx**](swbemservicesex.md) guarda un objeto de forma asincrónica en un espacio de nombres. Cuando se realiza correctamente, este método envía un evento [**alcompleto**](swbemsink-oncompleted.md) al objeto [**SWbemSink**](swbemsink.md) que se especifica como parámetro de entrada.

Se llama a este método en el modo asincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obligatorio. Receptor de objeto que recibe los objetos de forma asincrónica. Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.

</dd> <dt>

*ojbWbemObject* 
</dt> <dd>

Obligatorio. Nuevo objeto que se va a colocar en el espacio de nombres. Puede tratarse de un objeto recién creado o de un objeto modificado.

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Este parámetro determina si la llamada crea o actualiza el objeto y si la llamada se devuelve inmediatamente. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0X0))


</dt> <dd>

Permite actualizar una clase cuando no hay clases derivadas ni instancias para la clase. También permite las actualizaciones en todos los casos en los que el cambio solo es a calificadores no importantes, por ejemplo, el calificador de **Descripción** . Éste es el comportamiento predeterminado de esta llamada y se utiliza para la compatibilidad con versiones anteriores de WMI. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))


</dt> <dd>

Permite actualizaciones de clases incluso cuando hay clases secundarias y el cambio no provoca conflictos con las clases secundarias. Utilice esta marca al agregar una nueva propiedad a una clase base que no se menciona previamente en ninguna de las clases secundarias. Si la clase tiene instancias, se produce un error en la actualización.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))


</dt> <dd>

Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto. Por ejemplo, esta marca fuerza una actualización cuando se define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador en conflicto con el existente. En el modo Force, este conflicto se resuelve eliminando el calificador en conflicto de la clase secundaria. Si la clase tiene instancias, se produce un error en la actualización.

El uso del modo Force para actualizar una clase estática provoca la eliminación de todas las instancias de esa clase. Una actualización forzada en una clase de proveedor no elimina las instancias de la clase.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0X0))


</dt> <dd>

Hace que se cree la clase o instancia si no existe o se sobrescribe si ya existe.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0X2))


</dt> <dd>

Se usa solo para creación. Se produce un error en la llamada si la clase o la instancia ya existe.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))


</dt> <dd>

Hace que esta llamada se actualice. La clase o instancia debe existir para que la llamada sea correcta.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Hace que la llamada se devuelva inmediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0X0))


</dt> <dd>

Hace que esta llamada se bloquee hasta que se complete la consulta. Esta marca llama al método en el modo sincrónico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que WMI escriba los datos de modificación de clase y la definición de clase base. Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opta\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ opta\]
</dt> <dd>

Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obtener más información, consulte [llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si la llamada se realiza correctamente, el evento [**OnObjectPut**](swbemsink-onobjectput.md) del receptor del objeto proporcionado recibe un objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contiene la ruta de acceso del objeto de la instancia o la clase que se confirma correctamente en WMI.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **PutAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para actualizar una instancia de la clase especificada.

</dd> <dt>

**wbemErrAlreadyExists** -2147749913 (0x80041019)
</dt> <dd>

Se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrIllegalNull** -2147749898 (0x8004100A)
</dt> <dd>

Se especificó un valor null para una propiedad que no puede ser null. Un ejemplo de este tipo de propiedad está marcado por un calificador de **clave**, **indexado** o **no \_ null** .

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

La instancia especificada no es válida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Se especificó la marca **wbemChangeFlagUpdateOnly** , pero la instancia o la clase no existen.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

No se han establecido todas las propiedades requeridas para las clases.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta llamada se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor que se especifica en *objWbemSink*. Para controlar cada objeto cuando llega, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Cualquier procesamiento realizado después de que lleguen todos los objetos se realiza en una subrutina de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | \_ISWBEMSERVICESEX IID<br/>                                                        |



 

