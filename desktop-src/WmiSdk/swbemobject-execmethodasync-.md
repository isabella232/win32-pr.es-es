---
description: El método ExecMethodAsync de SWbemObject ejecuta de forma asincrónica un \_ método que exporta un proveedor de métodos.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_ método (Wbemdisp.h)
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
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857355"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exemétodo \_ cMethodAsync

El **método ExecMethodAsync \_** de [**SWbemObject**](swbemobject.md) ejecuta de forma asincrónica un método que exporta un proveedor de métodos. Este método es similar [**aSWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), pero funciona directamente en el objeto del método que se va a ejecutar. Windows Instrumental de administración (WMI) no implementa este método. El proveedor implementa este método.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*objWbemSink* \[ En\]
</dt> <dd>

Obligatorio. Este es el receptor de objetos que recibe los resultados de la llamada al método . Los parámetros de salida se envían al [**evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del receptor del objeto proporcionado. Los resultados del mecanismo de llamada se envían al evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del receptor del objeto proporcionado. Observe que **SWbemSink.OnCompleted** no recibe el código de retorno del método . Sin embargo, recibe el código de retorno del mecanismo de devolución de llamadas real y solo es útil para comprobar que se produjo la llamada o que se produjo un error por motivos mecánicos. El código de resultado devuelto por el método se devuelve en el objeto de parámetro de salida proporcionado a **SWbemSink.OnObjectReady**. Si se devuelve algún código de error, no se usa el objeto [**IWbemObjectSink**](iwbemobjectsink.md) proporcionado. Si la llamada se realiza correctamente, se llama a la implementación **IWbemObjectSink** del usuario para indicar el resultado de la operación.

</dd> <dt>

*strMethodName* \[ En\]
</dt> <dd>

Obligatorio. Este es el nombre del método para el objeto .

</dd> <dt>

*objwbemInParams* \[ in, opcional\]
</dt> <dd>

Se trata de [**un objeto SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta. De forma predeterminada, este parámetro no está definido. Para obtener más información, [vea Construir objetos InParameters](constructing-inparameters-objects.md) y [Analizar objetos OutParameters](parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Entero que determina el comportamiento de la llamada. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ in, opcional\]
</dt> <dd>

Se trata de [**un objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no tiene valores devueltos. Si la llamada se realiza correctamente, se proporciona un objeto [**OutParameters,**](swbemmethod-outparameters.md) que también es un objeto [**SWbemObject,**](swbemobject.md) al receptor especificado en *objWbemSink*. El objeto **OutParameters** devuelto contiene los parámetros de salida y el valor devuelto para el método que se ejecuta.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método ExecMethodAsync, \_** el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass:** 2147749904 (0x80041010)
</dt> <dd>

La clase especificada no era válida.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrInvalidMethod:** 2147749934 (0x8004102E)
</dt> <dd>

El método solicitado no estaba disponible.

</dd> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no estaba autorizado para ejecutar el método .

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use el **SWbemObject.Exemétodo cMethodAsync \_** como alternativa al acceso [](gloss-p.md) directo para ejecutar un método de proveedor cuando no se pueda ejecutar un método directamente. Por ejemplo, si el método tiene parámetros out, use el método **SWbemObject.ExecMethodAsync \_** con un lenguaje de scripting que no admita parámetros de salida. De lo contrario, se recomienda invocar un método mediante el acceso directo. Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada a través de devoluciones de llamada entregadas al receptor especificado en *objWbemSink*. Para procesar cada objeto cuando llega, cree *un objWbemSink*. [**Subrutina de eventos OnObjectReady.**](swbemsink-onobjectready.md) Una vez devueltos todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincrónica o la comunicación sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Si el método que se ejecuta tiene parámetros de entrada, el objeto [**InParameters**](swbemmethod-inparameters.md) y el parámetro *objWbemInParam* deben construirse como se describe en Construcción de objetos [InParameters](constructing-inparameters-objects.md) y Análisis de [objetos OutParameters](parsing-outparameters-objects.md).

El **SWbemObject.Exemétodo \_ cMethodAsync** da por supuesto que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar. El [**SWbemServices.Exemétodo cMethodAsync**](swbemservices-execmethodasync.md) requiere una ruta de acceso de objeto.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra [**el método ExecMethodAsync.**](swbemservices-execmethodasync.md) El script crea un [**objeto Process \_ de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que se ejecuta Bloc de notas. Muestra la configuración del objeto [**InParameters**](swbemmethod-inparameters.md) y cómo obtener resultados de un [**objeto OutParameters.**](swbemmethod-outparameters.md)

Para obtener un script que muestre las mismas operaciones realizadas sincrónicamente, [**veaSWbemObject.ExecMethod**](swbemobject-execmethod-.md). Para obtener un ejemplo de uso del acceso directo, [**vea Create Method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obtener un ejemplo de la misma operación mediante [**un objeto SWbemServices,**](swbemservices.md) [**veaSWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

