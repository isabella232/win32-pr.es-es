---
description: Ejecuta un método exportado por un proveedor de métodos.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082754"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Exemétodo cMethod

El método **ExecMethod** del objeto [**SWbemServices**](swbemservices.md) ejecuta un método exportado por un proveedor de métodos. Este método se bloquea mientras se ejecuta el método que se reenvía al proveedor adecuado. A continuación, se devuelven la información y el estado. El proveedor, en lugar de WMI, implementa el método.

Se llama a este método en el modo sincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método. Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obligatorio. Nombre del método para el objeto.

</dd> <dt>

*objWbemInParams* \[ opta\]
</dt> <dd>

Un objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se está ejecutando. De forma predeterminada, este parámetro es indefinido. Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Reservado. Este valor debe ser cero.

</dd> <dt>

*objWbemNamedValueSet* \[ opta\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, se devuelve un objeto [**SWbemObject**](swbemobject.md) . El objeto devuelto contiene los parámetros de salida y el valor devuelto para el método que se está ejecutando.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecMethod** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

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

Use **SWbemServices.ExecMethod** como alternativa al acceso directo para ejecutar un método de [*proveedor*](gloss-p.md) en los casos en los que no es posible ejecutar un método directamente. El método **ExecMethod** permite obtener parámetros de salida, si el proveedor los proporciona, con un lenguaje de scripting que no admite parámetros de salida. De lo contrario, el medio recomendado para invocar un método es usar el acceso directo. Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

Por ejemplo, el siguiente ejemplo de código que llama al método de proveedor de [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) utiliza el acceso directo.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



En este ejemplo se llama a **SWbemServices.ExecMethod** para ejecutar el método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Tenga en cuenta que se requiere una ruta de acceso al objeto porque **SWbemServices.ExecMethod** no funciona en el objeto, a diferencia de [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



El método **cMethodSWbemServices.Exe** requiere una ruta de acceso al objeto. Si el script ya contiene un objeto [**SWbemObject**](swbemobject.md) , use el método [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el método **ExecMethod** . El script crea un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas. Muestra la configuración de un objeto [**Parameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de un objeto [**Parameters**](swbemmethod-outparameters.md) . Para obtener un script que muestra las mismas operaciones que se realizaron de forma asincrónica, vea [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Para obtener un ejemplo del uso de acceso directo, consulte [Create method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obtener un ejemplo de la misma operación con un [**SWbemObject**](swbemobject.md), vea [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
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
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[Llamar a un método de proveedor](calling-a-provider-method.md)
</dt> <dt>

[Manipular información de clase e instancia](manipulating-class-and-instance-information.md)
</dt> </dl>

 

