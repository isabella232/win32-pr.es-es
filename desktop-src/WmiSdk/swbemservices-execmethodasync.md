---
description: 'SWbemServices.Exemétodo cMethodAsync: ejecuta un método exportado por un proveedor de métodos.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethodAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105593"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.Exemétodo cMethodAsync

El **método ExecMethodAsync** del objeto [**SWbemServices**](swbemservices.md) ejecuta un método exportado por un proveedor de métodos. La llamada vuelve inmediatamente al cliente mientras los parámetros de entrada se reenvía al proveedor adecuado donde se ejecuta el método. La información y el estado se devuelven al autor de la llamada a través de eventos entregados al receptor que se especifica en *objWbemSink*. El proveedor, en lugar Instrumental de administración de Windows (WMI), implementa el método .

Se llama al método en modo asincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener más información y una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Necesario. Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos. Receptor de objeto que recibe el resultado de la llamada al método. Los parámetros de salida se envían al [**evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del receptor de objetos proporcionado. Los resultados del mecanismo de llamada se envían al evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del receptor de objetos proporcionado. Tenga en cuenta **que SWbemSink.OnCompleted** no recibe el código de retorno del método WMI. Sin embargo, recibe el código de retorno del mecanismo de devolución de llamadas real y solo es útil para comprobar que la llamada se produjo o que se produjo un error por motivos mecánicos. El código de resultado que se devuelve del método WMI se devuelve en el objeto de parámetro de salida proporcionado a **SWbemSink.OnObjectReady**. Si se devuelve algún código de error, no se usa el objeto [**IWbemObjectSink**](iwbemobjectsink.md) proporcionado. Si la llamada se realiza correctamente, se llama a la implementación **IWbemObjectSink** del usuario para indicar el resultado de la operación.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Necesario. Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Necesario. Nombre del método que se va a ejecutar.

</dd> <dt>

*objWbemInParams* \[ Opcional\]
</dt> <dd>

Objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta. De forma predeterminada, este parámetro no está definido. Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Entero que determina el comportamiento de la llamada. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Realizar una llamada asincrónica con VBScript.](making-an-asynchronous-call-with-vbscript.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si la llamada se realiza correctamente, se proporciona un objeto [**OutParameters,**](swbemmethod-outparameters.md) que también es [**un objeto SWbemObject**](swbemobject.md) al receptor especificado en *objWbemSink*. El objeto **OutParameters** devuelto contiene los parámetros de salida y el valor devuelto para el método que se ejecuta. Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecMethodAsync,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error enumerados en la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass** : 2147749904 (0x80041010)
</dt> <dd>

La clase especificada no era válida.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory-** 2147749894 (0x80041006)
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

Si el método ejecutado tiene parámetros de entrada, el objeto [**InParameters**](swbemmethod-inparameters.md) del parámetro *objWbemInParam* debe ser el mismo que la descripción de los temas Construcción de objetos InParameters y Análisis de [objetos OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

Use **SWbemServices.ExecMethodAsync** como alternativa al acceso directo [](gloss-p.md) para ejecutar un método de proveedor cuando no sea posible ejecutar un método directamente. Por ejemplo, úselo con un lenguaje de scripting que no admita parámetros de salida, es decir, si el método tiene parámetros OUT. De lo contrario, se recomienda usar el acceso directo para invocar un método. Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

El **SWbemServices.ExecMethodAsync** requiere una ruta de acceso de objeto. Si el script ya contiene un [**objeto SWbemObject,**](swbemobject.md) puede llamar a [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).

Esta llamada se devuelve inmediatamente. La información de estado se devuelve al autor de la llamada a través de las llamadas devueltas al receptor que se especifica en *objWbemSink*. Para continuar el procesamiento cuando se complete la llamada, implemente una subrutina para *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para obtener más información sobre cómo eliminar los riesgos, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

Use el *parámetro objWbemAsyncContext* para comprobar el origen de una llamada.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra **el método ExecMethodAsync.** El script crea un [**objeto Proceso de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas. Muestra la configuración de un objeto [**InParameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de [**un objeto OutParameters.**](swbemmethod-outparameters.md) Para obtener un script que muestre las mismas operaciones realizadas sincrónicamente, [**veaSWbemServices.ExecMethod**](swbemservices-execmethod.md). Para obtener un ejemplo del uso del acceso directo, vea [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obtener un ejemplo de la misma operación [**mediante SWbemObject**](swbemobject.md), [**veaSWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Llamar a un método provider](calling-a-provider-method.md)
</dt> <dt>

[Manipulación de la información de clase e instancia](manipulating-class-and-instance-information.md)
</dt> </dl>

 

