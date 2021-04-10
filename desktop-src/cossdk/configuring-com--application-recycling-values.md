---
description: Puede usar los métodos siguientes para configurar los valores de reciclaje de la aplicación para la aplicación COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configuración de los valores de reciclaje de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153467"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="a6f11-103">Configuración de los valores de reciclaje de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="a6f11-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="a6f11-104">Puede usar los métodos siguientes para configurar los valores de reciclaje de la aplicación para la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="a6f11-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="a6f11-105">No se puede reciclar una aplicación COM+ que se ha configurado para ejecutarse como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="a6f11-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="a6f11-106">Además, las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.</span><span class="sxs-lookup"><span data-stu-id="a6f11-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a6f11-107">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="a6f11-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="a6f11-108">Para configurar el reciclaje de aplicaciones para una aplicación COM+, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a6f11-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="a6f11-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación de servidor COM+ que desea reciclar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="a6f11-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="a6f11-110">En la pestaña **agrupación & reciclaje** , escriba los valores de **límite de duración (minutos)**, límite de **memoria (KB)**, **tiempo de espera de expiración (minutos)**, **límite de llamadas** y **límite de activaciones**, en función de los criterios que desee utilizar.</span><span class="sxs-lookup"><span data-stu-id="a6f11-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="a6f11-111">**Límite de duración** indica el número máximo de minutos que puede ejecutarse un proceso antes de que se recicle.</span><span class="sxs-lookup"><span data-stu-id="a6f11-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="a6f11-112">El intervalo válido es de 0 a 30.240 minutos (21 días).</span><span class="sxs-lookup"><span data-stu-id="a6f11-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="a6f11-113">El número predeterminado de minutos es 0.</span><span class="sxs-lookup"><span data-stu-id="a6f11-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="a6f11-114">**Límite de memoria** indica la cantidad máxima de uso de memoria de proceso (en kilobytes) antes de reciclar el proceso.</span><span class="sxs-lookup"><span data-stu-id="a6f11-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="a6f11-115">Si el uso de memoria del proceso excede el número especificado durante más de un minuto, el proceso se recicla.</span><span class="sxs-lookup"><span data-stu-id="a6f11-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="a6f11-116">El intervalo válido es de 0 a 1.048.576 KB y el uso de memoria predeterminado es de 0 KB.</span><span class="sxs-lookup"><span data-stu-id="a6f11-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="a6f11-117">El **tiempo de espera de expiración** indica el número de minutos que se debe esperar antes de que se cierre forzosamente, para la liberación de todas las referencias externas a los objetos del proceso.</span><span class="sxs-lookup"><span data-stu-id="a6f11-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="a6f11-118">El intervalo válido es de 1 a 1440 minutos (24 horas) y el tiempo de espera de expiración predeterminado es 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="a6f11-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="a6f11-119">Este valor sólo se usa cuando ya se ha determinado que un proceso se reciclará en función de otros criterios.</span><span class="sxs-lookup"><span data-stu-id="a6f11-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="a6f11-120">**Límite de llamadas** indica el número máximo de llamadas que los objetos de aplicación pueden aceptar antes de reciclar el proceso.</span><span class="sxs-lookup"><span data-stu-id="a6f11-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="a6f11-121">El intervalo válido es de 0 a 1.048.576 llamadas y el número predeterminado de llamadas es 0.</span><span class="sxs-lookup"><span data-stu-id="a6f11-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="a6f11-122">**Límite de activación** indica el número máximo de activaciones de objetos de aplicación que se aceptan antes de reciclar el proceso.</span><span class="sxs-lookup"><span data-stu-id="a6f11-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="a6f11-123">El intervalo válido es de 0 a 1.048.576 activaciones y el número predeterminado de activaciones es 0.</span><span class="sxs-lookup"><span data-stu-id="a6f11-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="a6f11-124">Cuando el valor de límite de **duración**, **límite de memoria**, **límite de llamadas** o límite de **activación** se establece en 0 (el valor predeterminado), se deshabilita el reciclaje de la aplicación para ese criterio.</span><span class="sxs-lookup"><span data-stu-id="a6f11-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="a6f11-125">Cuando los cuatro criterios se establecen en 0, el reciclaje de la aplicación está deshabilitado para la aplicación seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a6f11-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="a6f11-126">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6f11-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a6f11-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a6f11-127">Visual Basic</span></span>

<span data-ttu-id="a6f11-128">La siguiente función de Microsoft Visual Basic muestra cómo puede establecer los valores de reciclaje de la aplicación para cualquier aplicación de servidor COM+ que elija.</span><span class="sxs-lookup"><span data-stu-id="a6f11-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="a6f11-129">Para usarlo desde Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="a6f11-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="a6f11-130">Para usar la función, proporcione un valor de cadena para el nombre de la aplicación y valores enteros para la configuración de reciclaje de la aplicación deseada.</span><span class="sxs-lookup"><span data-stu-id="a6f11-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="a6f11-131">En el siguiente código de Visual Basic se muestra cómo establecer el valor de **RecycleLifetimeLimit** en 5, el valor de **RecycleMemoryLimit** en 10, el valor de **RecycleCallLimit** en 9, el valor de **RecycleActivationLimit** en 100 y el valor de **RecycleExpirationTimeout** en 15.</span><span class="sxs-lookup"><span data-stu-id="a6f11-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="a6f11-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6f11-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f11-133">Conceptos de reciclaje de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="a6f11-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



