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
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="d1655-103">Registrar una devolución de llamada en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d1655-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="d1655-104">Agregar una devolución de llamada en Visual Basic es diferente del método usado en VBScript.</span><span class="sxs-lookup"><span data-stu-id="d1655-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="d1655-105">La función **GetRef** utilizada en VBScript es diferente de la que se usa en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d1655-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="d1655-106">Por lo tanto, un desarrollador debe crear un objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenga la función de devolución de llamada como método predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d1655-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="d1655-107">En este tema se proporciona la información necesaria para desarrollar aplicaciones Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d1655-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="d1655-108">**Para implementar esta devolución de llamada en una aplicación**</span><span class="sxs-lookup"><span data-stu-id="d1655-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="d1655-109">Agregue referencias a dos bibliotecas de objetos: TLBTypes. olb y VboostTypes6. olb.</span><span class="sxs-lookup"><span data-stu-id="d1655-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="d1655-110">Estas bibliotecas de objetos se proporcionan con el código de ejemplo del punto de control.</span><span class="sxs-lookup"><span data-stu-id="d1655-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="d1655-111">Agregue una referencia a Cbklib. tlb.</span><span class="sxs-lookup"><span data-stu-id="d1655-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="d1655-112">Este archivo define la estructura de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d1655-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="d1655-113">Cbklib. tlb se crea mediante el archivo cbklib. idl que se incluye como parte del código de ejemplo de punto de control.</span><span class="sxs-lookup"><span data-stu-id="d1655-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="d1655-114">Se recomienda que el nombre de este archivo cambie para las funciones de devolución de llamada que difieren en la estructura de sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="d1655-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="d1655-115">En este ejemplo se usa MIDL para crear el archivo de biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="d1655-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="d1655-116">Escriba la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d1655-116">Write the callback function.</span></span> <span data-ttu-id="d1655-117">Los parámetros son los mismos que en el ejemplo de VBScript del [registro de una devolución de llamada](registering-a-callback.md).</span><span class="sxs-lookup"><span data-stu-id="d1655-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="d1655-118">En este ejemplo se imprime una cadena cada vez que llega un evento.</span><span class="sxs-lookup"><span data-stu-id="d1655-118">This example prints a string whenever an event arrives.</span></span>
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

    

4.  <span data-ttu-id="d1655-119">Agregue la función de devolución de llamada al objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , como se muestra en el ejemplo siguiente, o en otro objeto como [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), mediante la biblioteca de tipos de devolución de llamada adecuada (cbklib. TBL).</span><span class="sxs-lookup"><span data-stu-id="d1655-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
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

    

<span data-ttu-id="d1655-120">En el ejemplo siguiente, el objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="d1655-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="d1655-121">A continuación, la función de devolución de llamada se agrega como parámetro.</span><span class="sxs-lookup"><span data-stu-id="d1655-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="d1655-122">Bibliotecas de objetos usadas en el código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1655-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="d1655-123">Los ejemplos anteriores y el código de ejemplo de punto de control usan algunas de las siguientes bibliotecas de objetos:</span><span class="sxs-lookup"><span data-stu-id="d1655-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="d1655-124">TLBTypes. olb: esta biblioteca define algunos de los tipos de biblioteca de tipos e interfaces que se usan en el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d1655-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="d1655-125">Define algunas de las funciones que se van a usar en Visual Basic, como [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), que ya están disponibles en C o C++.</span><span class="sxs-lookup"><span data-stu-id="d1655-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="d1655-126">VboostTypes6. olb: esta biblioteca define algunos tipos base que se usan en TLBTypes. olb y FunctionDelegator. Bas. Puede encontrar más información sobre TLBTypes en el libro *Advanced Visual Basic 6: técnicas de energía para programas cotidianos*, mediante Matthew Curland (Addison-Wesley, julio 2000, ISBN: 0-201-70712-8).</span><span class="sxs-lookup"><span data-stu-id="d1655-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="d1655-127">(Es posible que este libro no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="d1655-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="d1655-128">El código de ejemplo de punto de control y las siguientes bibliotecas están relacionados con esta sección y son necesarios para implementar esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d1655-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="d1655-129">Se pueden encontrar con el código de ejemplo de punto de control:</span><span class="sxs-lookup"><span data-stu-id="d1655-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="d1655-130">Cbklib. idl</span><span class="sxs-lookup"><span data-stu-id="d1655-130">Cbklib.idl</span></span>
-   <span data-ttu-id="d1655-131">Cbklib. tlb</span><span class="sxs-lookup"><span data-stu-id="d1655-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="d1655-132">VboostTypes6. olb</span><span class="sxs-lookup"><span data-stu-id="d1655-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="d1655-133">TLBTypes. olb</span><span class="sxs-lookup"><span data-stu-id="d1655-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="d1655-134">FunctionDelegator. Bas</span><span class="sxs-lookup"><span data-stu-id="d1655-134">FunctionDelegator.bas</span></span>

 

 