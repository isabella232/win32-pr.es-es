---
description: El \_ método ExecMethodAsync de SWbemObject ejecuta de forma asincrónica un método que exporta un proveedor de métodos.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Método de cMethodAsync_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278975"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exe\_ método cMethodAsync

El **método \_ ExecMethodAsync** de [**SWbemObject**](swbemobject.md) ejecuta de forma asincrónica un método que exporta un proveedor de métodos. Este método es similar a [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), pero funciona directamente en el objeto del método que se va a ejecutar. Instrumental de administración de Windows (WMI) no implementa este método. El proveedor implementa este método.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* \[ de\]
</dt> <dd>

Obligatorio. Es el receptor del objeto que recibe los resultados de la llamada al método. Los parámetros de salida se envían al evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del receptor de objeto proporcionado. Los resultados del mecanismo de llamada se envían al evento [**SWbemSink. Alcompleted**](swbemsink-oncompleted.md) del receptor de objetos proporcionado. Tenga en cuenta que **SWbemSink. Alcompleted** no recibe el código de retorno del método. Sin embargo, recibe el código de retorno del mecanismo de devolución de llamada real y solo es útil para comprobar que se ha producido la llamada, o que se ha producido un error por motivos mecánicos. El código de resultado devuelto por el método se devuelve en el objeto de parámetro saliente proporcionado a **SWbemSink. OnObjectReady**. Si se devuelve algún código de error, no se utiliza el objeto [**IWbemObjectSink**](iwbemobjectsink.md) proporcionado. Si la llamada se realiza correctamente, se llama a la implementación de **IWbemObjectSink** del usuario para indicar el resultado de la operación.

</dd> <dt>

*strMethodName* \[ de\]
</dt> <dd>

Obligatorio. Es el nombre del método para el objeto.

</dd> <dt>

*objwbemInParams* \[ en, opcional\]
</dt> <dd>

Este es un objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se está ejecutando. De forma predeterminada, este parámetro es indefinido. Para obtener más información, consulte [construir objetos Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Entero que determina el comportamiento de la llamada. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0X0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Normalmente, es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ en, opcional\]
</dt> <dd>

Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obtener más información, consulte [llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no tiene ningún valor devuelto. Si la llamada es correcta, se proporciona un objeto [**Parameters**](swbemmethod-outparameters.md) , que también es un objeto [**SWbemObject**](swbemobject.md) , al receptor especificado en *objWbemSink*. El objeto **Parameters** devuelto contiene los parámetros de salida y el valor devuelto para el método que se está ejecutando.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ ExecMethodAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La clase especificada no era válida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E)
</dt> <dd>

El método solicitado no estaba disponible.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El usuario actual no está autorizado para ejecutar el método.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el método **SWbemObject.Exe\_ cMethodAsync** como alternativa al acceso directo para ejecutar un método de [*proveedor*](gloss-p.md) cuando no se puede ejecutar un método directamente. Por ejemplo, si el método tiene parámetros out, utilice el método **SWbemObject.Exe\_ cMethodAsync** con un lenguaje de scripting que no admita parámetros de salida. De lo contrario, se recomienda invocar un método mediante el acceso directo. Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*. Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

Si el método que se ejecuta tiene parámetros de entrada, el objeto [**Parameters**](swbemmethod-inparameters.md) y el parámetro *objWbemInParam* se deben construir tal y como se describe en construir objetos [Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).

En el método **\_ cMethodAsyncSWbemObject.Exe** se supone que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar. El método [**cMethodAsyncSWbemServices.Exe**](swbemservices-execmethodasync.md) requiere una ruta de acceso al objeto.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el método [**ExecMethodAsync**](swbemservices-execmethodasync.md) . El script crea un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas. Muestra cómo configurar el objeto [**Parameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de un objeto [**Parameters**](swbemmethod-outparameters.md) .

Para obtener un script que muestra las mismas operaciones realizadas sincrónicamente, vea [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md). Para obtener un ejemplo de uso de acceso directo, consulte [**Create method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obtener un ejemplo de la misma operación mediante un objeto [**SWbemServices**](swbemservices.md) , vea [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

