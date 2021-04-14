---
description: Información general de los controles de entrada manuscrita para Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controles de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541315"
---
# <a name="ink-controls"></a><span data-ttu-id="812f3-103">Controles de entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="812f3-103">Ink Controls</span></span>

<span data-ttu-id="812f3-104">La plataforma de Tablet PC proporciona dos controles, [InkEdit](inkedit-control.md) y [InkPicture](inkpicture-control.md), que le permiten agregar fácilmente reconocimiento de tinta y escritura a mano a las aplicaciones de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="812f3-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="812f3-105">El control InkEdit tiene versiones [administradas](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) y Win32, mientras que InkPicture solo tiene las versiones de [InkPicture](/previous-versions/ms583740(v=vs.100)) y [ActiveX](inkpicture-control-reference.md) administradas.</span><span class="sxs-lookup"><span data-stu-id="812f3-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="812f3-106">La diferencia clave entre los controles es cómo se guardan los datos.</span><span class="sxs-lookup"><span data-stu-id="812f3-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="812f3-107">El control [InkEdit](inkedit-control.md) guarda la entrada manuscrita como texto de forma predeterminada, mientras que [InkPicture](inkpicture-control.md) guarda la tinta como entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="812f3-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="812f3-108">El control [InkEdit](inkedit-control.md) está destinado a la entrada de texto mediante el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="812f3-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="812f3-109">El formato de [InkPicture](inkpicture-control.md) está diseñado para la anotación (por ejemplo, al marcar una diapositiva de presentación u otra imagen).</span><span class="sxs-lookup"><span data-stu-id="812f3-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="812f3-110">En código administrado, cree controles de entrada de lápiz en el mismo subproceso que el subproceso principal del formulario.</span><span class="sxs-lookup"><span data-stu-id="812f3-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="812f3-111">Si se crea un control [InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) en un subproceso diferente, es posible que la aplicación no responda correctamente.</span><span class="sxs-lookup"><span data-stu-id="812f3-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="812f3-112">Debe cambiar explícitamente el modelo de subprocesos a Apartamento de un solo subproceso (STA) antes de crear un control de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="812f3-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="812f3-113">Esto hace que el control se cree en el subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="812f3-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="812f3-114">Puede usar el siguiente código de C++ administrado para establecer explícitamente el modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="812f3-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="812f3-115">Puede usar el siguiente código para hacer lo mismo en C \# .</span><span class="sxs-lookup"><span data-stu-id="812f3-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="812f3-116">En código administrado, para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el control salga del ámbito.</span><span class="sxs-lookup"><span data-stu-id="812f3-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="812f3-117">En las secciones siguientes se describen los controles de entrada manuscrita y el uso de controles de entrada manuscrita en aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="812f3-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="812f3-118">Agregar controles de entrada manuscrita a un proyecto</span><span class="sxs-lookup"><span data-stu-id="812f3-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="812f3-119">Control InkEdit</span><span class="sxs-lookup"><span data-stu-id="812f3-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="812f3-120">InkPicture (control)</span><span class="sxs-lookup"><span data-stu-id="812f3-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
