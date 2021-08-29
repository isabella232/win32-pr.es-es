---
description: El método ExecMethod \_ del objeto SWbemObject ejecuta un método exportado por un proveedor de métodos.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: SWbemObject.ExecMethod_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5cc743d369e8ecccd7691710bb82373270d6e58736a173bbf3b4f1d15af548c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857365"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Exemétodo \_ cMethod

El **método \_ ExecMethod** del [**objeto SWbemObject**](swbemobject.md) ejecuta un método exportado por un proveedor de métodos.

Este método se detiene mientras se ejecuta el método que se reenvía al proveedor adecuado. A continuación, se devuelve la información y el estado. El proveedor en lugar de WMI implementa el método .

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strMethodName* \[ En\]
</dt> <dd>

Obligatorio. Nombre del método para el objeto .

</dd> <dt>

*objwbemInParams* \[ in, opcional\]
</dt> <dd>

Se trata de [**un objeto SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta. De forma predeterminada, este parámetro no está definido. Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado y debe establecerse en 0 (cero) si se especifica.

</dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método es correcto, devuelve [**un objeto SWbemObject.**](swbemobject.md) El objeto devuelto contiene los parámetros out y el valor devuelto para el método que se ejecuta.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **\_ ExecMethod,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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

Este método es similar [**aSWbemServices.ExecMethod**](swbemservices-execmethod.md), pero funciona directamente en el objeto cuyo método se va a ejecutar. Por ejemplo, en el ejemplo de código siguiente se llama [**al método del proveedor StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) y se usa [el acceso directo](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Esta versión llama **SWbemObject.ExecMethod para \_** ejecutar el método [**StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Use **SWbemObject.ExecMethod \_** como alternativa al acceso directo [](gloss-p.md) para ejecutar un método de proveedor en casos en los que no sea posible ejecutar un método directamente. Por ejemplo, usaríaSWbemObject.Exe **cMethod \_** con un lenguaje de scripting que no admita parámetros de salida si el método tiene parámetros out. De lo contrario, el medio recomendado para invocar un método es usar el acceso directo.

-   El **SWbemObject.ExecMethod \_ da** por supuesto que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar. Por el contrario, [**SWbemServices.ExecMethod requiere**](swbemservices-execmethod.md) una ruta de acceso de objeto. Use **SWbemObject.ExecMethod \_** si ya ha obtenido el objeto cuyo método desea ejecutar.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra [**el método ExecMethod.**](swbemservices-execmethod.md) El script crea un objeto [**Process de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que se ejecuta Bloc de notas. Para obtener más información sobre un script que ilustra las mismas operaciones realizadas de forma asincrónica, [**veaSWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md). Para obtener un ejemplo de uso del acceso directo, [**vea Create Method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Para obtener un ejemplo de la misma operación mediante [**un objeto SWbemServices,**](swbemservices.md) **veaSWbemServices.ExecMethod**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 

