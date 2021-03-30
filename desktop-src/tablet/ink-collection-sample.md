---
description: Esta aplicación se basa en el objeto InkCollector y muestra la colección de entradas de lápiz.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Ejemplo de colección de entradas manuscritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154185"
---
# <a name="ink-collection-sample"></a><span data-ttu-id="99c48-103">Ejemplo de colección de entradas manuscritas</span><span class="sxs-lookup"><span data-stu-id="99c48-103">Ink Collection Sample</span></span>

<span data-ttu-id="99c48-104">Esta aplicación se basa en el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) y muestra la colección de entradas de lápiz.</span><span class="sxs-lookup"><span data-stu-id="99c48-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="99c48-105">La aplicación crea una ventana, le adjunta un objeto InkCollector y proporciona al usuario opciones de menú que se pueden usar para cambiar el color de la tinta, el ancho de la tinta y habilitar y deshabilitar la recopilación de entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="99c48-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="99c48-106">La versión que se describe en esta sección es Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="99c48-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="99c48-107">Los conceptos son los mismos entre las versiones de otros lenguajes de la biblioteca de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="99c48-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="99c48-108">Declarar InkCollector</span><span class="sxs-lookup"><span data-stu-id="99c48-108">Declaring the InkCollector</span></span>

<span data-ttu-id="99c48-109">En primer lugar, la aplicación importa el espacio de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="99c48-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="99c48-110">A continuación, la aplicación declara `myInkCollector` , que contiene el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) del formulario.</span><span class="sxs-lookup"><span data-stu-id="99c48-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="99c48-111">Configuración de elementos</span><span class="sxs-lookup"><span data-stu-id="99c48-111">Setting Things Up</span></span>

<span data-ttu-id="99c48-112">El método del formulario `InkCollection_Load` controla el evento de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="99c48-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="99c48-113">Crea un objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) asignado al formulario modifica la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector y habilita el objeto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="99c48-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



<span data-ttu-id="99c48-114">[InkCollector](/previous-versions/ms836493(v=msdn.10)) se asigna a la ventana del formulario mediante la asignación del identificador de ventana del formulario a la propiedad [Handle](/previous-versions/ms836504(v=msdn.10)) del objeto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="99c48-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="99c48-115">La colección de tintas se activa estableciendo la propiedad [Enabled](/previous-versions/ms836503(v=msdn.10)) del objeto InkCollector en **true**.</span><span class="sxs-lookup"><span data-stu-id="99c48-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="99c48-116">La propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) establece los atributos predeterminados que se asignan a un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="99c48-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="99c48-117">Para establecer atributos diferentes en un nuevo cursor, utilice la propiedad [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) del objeto [cursor](/previous-versions/ms839521(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="99c48-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="99c48-118">Para cambiar los atributos de dibujo de un solo trazo, use la propiedad [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="99c48-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="99c48-119">Cambiar las propiedades</span><span class="sxs-lookup"><span data-stu-id="99c48-119">Changing the Properties</span></span>

<span data-ttu-id="99c48-120">El resto de esta aplicación simple consta de controladores para las diversas selecciones de menú que el usuario puede realizar.</span><span class="sxs-lookup"><span data-stu-id="99c48-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="99c48-121">Por ejemplo, cuando el usuario elige cambiar el color de la tinta a rojo seleccionando rojo en el menú de entrada manuscrita, el color cambia mediante la propiedad [color](/previous-versions/ms837933(v=msdn.10)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) en el controlador de eventos del menú.</span><span class="sxs-lookup"><span data-stu-id="99c48-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="99c48-122">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="99c48-122">Closing the Form</span></span>

<span data-ttu-id="99c48-123">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="99c48-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
