---
title: Registrar una devolución de llamada en Visual Basic
description: Agregar una devolución de llamada en Visual Basic es diferente del método usado en VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149478"
---
# <a name="registering-a-callback-in-visual-basic"></a>Registrar una devolución de llamada en Visual Basic

Agregar una devolución de llamada en Visual Basic es diferente del método usado en VBScript. La función **GetRef** utilizada en VBScript es diferente de la que se usa en Visual Basic. Por lo tanto, un desarrollador debe crear un objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenga la función de devolución de llamada como método predeterminado. En este tema se proporciona la información necesaria para desarrollar aplicaciones Visual Basic.

**Para implementar esta devolución de llamada en una aplicación**

1.  Agregue referencias a dos bibliotecas de objetos: TLBTypes. olb y VboostTypes6. olb. Estas bibliotecas de objetos se proporcionan con el código de ejemplo del punto de control.
2.  Agregue una referencia a Cbklib. tlb. Este archivo define la estructura de la función de devolución de llamada.

    Cbklib. tlb se crea mediante el archivo cbklib. idl que se incluye como parte del código de ejemplo de punto de control. Se recomienda que el nombre de este archivo cambie para las funciones de devolución de llamada que difieren en la estructura de sus parámetros. En este ejemplo se usa MIDL para crear el archivo de biblioteca de tipos.

3.  Escriba la función de devolución de llamada. Los parámetros son los mismos que en el ejemplo de VBScript del [registro de una devolución de llamada](registering-a-callback.md). En este ejemplo se imprime una cadena cada vez que llega un evento.
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  Agregue la función de devolución de llamada al objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , como se muestra en el ejemplo siguiente, o en otro objeto como [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), mediante la biblioteca de tipos de devolución de llamada adecuada (cbklib. TBL).
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

En el ejemplo siguiente, el objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) se pasa a la función. A continuación, la función de devolución de llamada se agrega como parámetro.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Bibliotecas de objetos usadas en el código de ejemplo

Los ejemplos anteriores y el código de ejemplo de punto de control usan algunas de las siguientes bibliotecas de objetos:

1.  TLBTypes. olb: esta biblioteca define algunos de los tipos de biblioteca de tipos e interfaces que se usan en el código de ejemplo. Define algunas de las funciones que se van a usar en Visual Basic, como [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), que ya están disponibles en C o C++.
2.  VboostTypes6. olb: esta biblioteca define algunos tipos base que se usan en TLBTypes. olb y FunctionDelegator. Bas. Puede encontrar más información sobre TLBTypes en el libro *Advanced Visual Basic 6: técnicas de energía para programas cotidianos*, mediante Matthew Curland (Addison-Wesley, julio 2000, ISBN: 0-201-70712-8). (Es posible que este libro no esté disponible en algunos idiomas y países).

El código de ejemplo de punto de control y las siguientes bibliotecas están relacionados con esta sección y son necesarios para implementar esta devolución de llamada. Se pueden encontrar con el código de ejemplo de punto de control:

-   Cbklib. idl
-   Cbklib. tlb
-   VboostTypes6. olb
-   TLBTypes. olb
-   FunctionDelegator. Bas

 

 