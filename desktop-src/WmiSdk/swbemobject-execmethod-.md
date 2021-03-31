---
description: El \_ método ExecMethod del objeto SWbemObject ejecuta un método exportado por un proveedor de métodos.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Método de cMethod_ de SWbemObject.Exe(Wbemdisp. h)
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
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155829"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Exe\_ método cMethod

El **método \_ ExecMethod** del objeto [**SWbemObject**](swbemobject.md) ejecuta un método exportado por un proveedor de métodos.

Este método se pausa mientras se ejecuta el método que se reenvía al proveedor adecuado. A continuación, se devuelven la información y el estado. El proveedor en lugar de WMI implementa el método.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

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

*strMethodName* \[ de\]
</dt> <dd>

Obligatorio. Nombre del método para el objeto.

</dd> <dt>

*objwbemInParams* \[ en, opcional\]
</dt> <dd>

Este es un objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se está ejecutando. De forma predeterminada, este parámetro es indefinido. Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reserved y debe establecerse en 0 (cero) si se especifica.

</dd> <dt>

*objwbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Normalmente, es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, se devuelve un objeto [**SWbemObject**](swbemobject.md) . El objeto devuelto contiene los parámetros de salida y el valor devuelto para el método que se está ejecutando.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecMethod \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

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

Este método es similar a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), pero funciona directamente en el objeto cuyo método se va a ejecutar. Por ejemplo, en el ejemplo de código siguiente se llama al método de proveedor de [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) y se usa el [acceso directo](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Esta versión llama a **SWbemObject.Exe\_ cMethod** para ejecutar el método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Use **SWbemObject.ExecMethod \_** como alternativa al acceso directo para ejecutar un método de [*proveedor*](gloss-p.md) en los casos en los que no es posible ejecutar un método directamente. Por ejemplo, usaría **SWbemObject.ExecMethod \_** con un lenguaje de scripting que no admita parámetros de salida si el método tiene parámetros out. De lo contrario, el medio recomendado para invocar un método es usar el acceso directo.

-   En el método **\_ cMethodSWbemObject.Exe** se supone que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar. Por el contrario, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requiere una ruta de acceso de objeto. Use **SWbemObject.ExecMethod \_** si ya ha obtenido el objeto cuyo método desea ejecutar.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el método [**ExecMethod**](swbemservices-execmethod.md) . El script crea un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas. Para obtener más información sobre un script que ilustra las mismas operaciones que se realizan de forma asincrónica, vea [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md). Para obtener un ejemplo de uso de acceso directo, consulte [**Create method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Para obtener un ejemplo de la misma operación mediante un objeto [**SWbemServices**](swbemservices.md) , vea **SWbemServices.ExecMethod**.


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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 

