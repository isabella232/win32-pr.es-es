---
description: 'Método SWbemServices.ExecMethod: ejecuta un método exportado por un proveedor de métodos.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: Método SWbemServices.ExecMethod (Wbemdisp.h)
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
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465483"
---
# <a name="swbemservicesexecmethod-method"></a>Método SWbemServices.ExecMethod

El **método ExecMethod** del [**objeto SWbemServices**](swbemservices.md) ejecuta un método exportado por un proveedor de métodos. Este método se bloquea mientras se ejecuta el método que se reenvía al proveedor adecuado. A continuación, se devuelve la información y el estado. El proveedor, en lugar de WMI, implementa el método .

Se llama a este método en modo sincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Necesario. Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Necesario. Nombre del método para el objeto .

</dd> <dt>

*objWbemInParams* \[ Opcional\]
</dt> <dd>

Objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta. De forma predeterminada, este parámetro no está definido. Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Reservado. Este valor debe ser cero.

</dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, se [**devuelve un objeto SWbemObject.**](swbemobject.md) El objeto devuelto contiene los parámetros out y el valor devuelto para el método que se ejecuta.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ExecMethod,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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

## <a name="remarks"></a>Observaciones

Use **SWbemServices.ExecMethod** como alternativa al acceso [](gloss-p.md) directo para ejecutar un método de proveedor en casos en los que no sea posible ejecutar un método directamente. El **método ExecMethod** permite obtener parámetros de salida, si el proveedor los proporciona, con un lenguaje de scripting que no admite parámetros de salida. De lo contrario, el medio recomendado para invocar un método es usar el acceso directo. Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

Por ejemplo, el siguiente ejemplo de código que llama al [**método de proveedor StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) en el [**servicio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) usa el acceso directo.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



En este ejemplo se **llama a SWbemServices.ExecMethod para** ejecutar el método [**StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) Tenga en cuenta que se requiere una ruta de acceso de objeto porque **SWbemServices.ExecMethod** aún no funciona en el objeto, a diferencia [**de SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



El **método SWbemServices.ExecMethod** requiere una ruta de acceso de objeto. Si el script ya contiene un [**objeto SWbemObject,**](swbemobject.md) use el [**método SWbemObject.ExecMethod.**](swbemobject-execmethod-.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra **el método ExecMethod.** El script crea un [**objeto Process \_ de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que se ejecuta Bloc de notas. Muestra la configuración de un objeto [**InParameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de [**un objeto OutParameters.**](swbemmethod-outparameters.md) Para obtener un script que muestre las mismas operaciones realizadas de forma asincrónica, vea [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Para obtener un ejemplo del uso del acceso directo, vea [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obtener un ejemplo de la misma operación mediante [**SWbemObject**](swbemobject.md), vea [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


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

[Llamar a un método provider](calling-a-provider-method.md)
</dt> <dt>

[Manipulación de información de clase e instancia](manipulating-class-and-instance-information.md)
</dt> </dl>

 

