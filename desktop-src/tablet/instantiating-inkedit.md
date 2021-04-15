---
description: En este tema se describen las distintas maneras en las que puede crear instancias de un control InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Crear instancias de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497650"
---
# <a name="instantiating-inkedit"></a><span data-ttu-id="ff32e-103">Crear instancias de InkEdit</span><span class="sxs-lookup"><span data-stu-id="ff32e-103">Instantiating InkEdit</span></span>

<span data-ttu-id="ff32e-104">En este tema se describen las distintas maneras en las que puede crear instancias de un control [InkEdit](inkedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="ff32e-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="ff32e-105">Visual Basic .NET y C\#</span><span class="sxs-lookup"><span data-stu-id="ff32e-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="ff32e-106">Si está trabajando con Microsoft Visual Basic .NET o C \# , arrastre el control [InkEdit](./inkedit-control.md) desde el cuadro de herramientas de Visual Studio hasta el formulario o la página donde desee que aparezca el control.</span><span class="sxs-lookup"><span data-stu-id="ff32e-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="ff32e-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="ff32e-107">Win32/C++</span></span>

<span data-ttu-id="ff32e-108">El control [InkEdit](inkedit-control-reference.md) es una superclase del control Rich Edit 4,5 Win32 OLE incrustable.</span><span class="sxs-lookup"><span data-stu-id="ff32e-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="ff32e-109">Las aplicaciones Win32 crean una instancia del control [InkEdit](inkedit-control-reference.md) llamando a [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) y pasando InkEdit como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="ff32e-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="ff32e-110">INKEDIT se define en el. h.</span><span class="sxs-lookup"><span data-stu-id="ff32e-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="ff32e-111">Una vez creado el control, puede "hablar" con el control con los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff32e-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="ff32e-112">Los mensajes Rich Edit (EM \_ \* ) se pasan desde InkEdit a Rich Edit sin modificar; toda la funcionalidad de edición enriquecida existente está disponible.</span><span class="sxs-lookup"><span data-stu-id="ff32e-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="ff32e-113">Para crear un control [InkEdit](inkedit-control-reference.md) , llame a la función [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , especificando la clase de ventana InkEdit.</span><span class="sxs-lookup"><span data-stu-id="ff32e-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="ff32e-114">Use [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para registrar InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="ff32e-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="ff32e-115">Especifique la \_ constante definida por la clase INKEDIT para el parámetro de clase de ventana y use los estilos de ventana que se especifican en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff32e-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="ff32e-116">Crear una instancia de un control InkEdit de varias líneas</span><span class="sxs-lookup"><span data-stu-id="ff32e-116">Instantiating a Multiline InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="ff32e-117">Crear una instancia de un control Single-Line InkEdit</span><span class="sxs-lookup"><span data-stu-id="ff32e-117">Instantiating a Single-Line InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> <span data-ttu-id="ff32e-118">A diferencia de RichEdit, debe asegurarse de llamar a [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de crear el control [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ff32e-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="ff32e-119">Llame a [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) cuando se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff32e-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="ff32e-120">Después de llamar a CoUninitialize (), debe llamar a [FreeLibrary (s \_ hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para reducir el recuento de referencias en el archivo de InkEdit.dll.</span><span class="sxs-lookup"><span data-stu-id="ff32e-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="ff32e-121">Si usa el estilo de ventana [ \_ NOIME es](../controls/rich-edit-control-styles.md) , la compatibilidad con la corrección integrada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="ff32e-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="ff32e-122">Si no se especifica una ventana primaria, el control se crea como una ventana de nivel superior y \_ se agrega el estilo WS SYSMENU; de esta forma, también se deshabilita la compatibilidad con la corrección integrada.</span><span class="sxs-lookup"><span data-stu-id="ff32e-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff32e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff32e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff32e-124">Agregar controles de entrada manuscrita a un proyecto</span><span class="sxs-lookup"><span data-stu-id="ff32e-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
