---
title: Portabilidad de los contextos de dispositivo y formatos de píxel
description: Portabilidad de los contextos de dispositivo y formatos de píxel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- trasladar a OpenGL, píxeles
- Portabilidad de OpenGL, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665605"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="57049-105">Portabilidad de los contextos de dispositivo y formatos de píxel</span><span class="sxs-lookup"><span data-stu-id="57049-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="57049-106">Cada ventana de la implementación de Microsoft de OpenGL para Windows tiene su propio formato de píxel actual.</span><span class="sxs-lookup"><span data-stu-id="57049-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="57049-107">Un formato de píxel se define mediante una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="57049-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="57049-108">Dado que cada ventana tiene su propio formato de píxel, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto del dispositivo y, a continuación, se crea un contexto de representación de OpenGL para el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57049-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="57049-109">El contexto de representación utiliza automáticamente el formato de píxel de su contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57049-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="57049-110">El sistema de ventana X también utiliza una estructura de datos, **XVisualInfo**, para especificar las propiedades de los píxeles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="57049-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="57049-111">Las estructuras **XVisualInfo** contienen una estructura de datos **Visual** que describe cómo se usan los recursos de color en una pantalla concreta.</span><span class="sxs-lookup"><span data-stu-id="57049-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="57049-112">En el sistema de ventana X, **XVisualInfo** se usa para crear una ventana estableciendo la ventana en el formato de píxel que desee.</span><span class="sxs-lookup"><span data-stu-id="57049-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="57049-113">La estructura devuelta se usa para crear la ventana y un contexto de representación.</span><span class="sxs-lookup"><span data-stu-id="57049-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="57049-114">En Windows, primero se crea una ventana y se obtiene un identificador de un contexto de dispositivo (HDC) de la ventana.</span><span class="sxs-lookup"><span data-stu-id="57049-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="57049-115">A continuación, se usa HDC para establecer el formato de píxel para la ventana.</span><span class="sxs-lookup"><span data-stu-id="57049-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="57049-116">El contexto de representación usa el formato de píxel de la ventana.</span><span class="sxs-lookup"><span data-stu-id="57049-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="57049-117">En la tabla siguiente se comparan las funciones visuales del sistema de ventanas X y GLX con sus funciones de formato de Windows píxeles equivalentes.</span><span class="sxs-lookup"><span data-stu-id="57049-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="57049-118">X Window/GLX función visual)</span><span class="sxs-lookup"><span data-stu-id="57049-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="57049-119">Función de formato de Windows píxeles</span><span class="sxs-lookup"><span data-stu-id="57049-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57049-120">XVisualInfo \* **glXChooseVisual**(Mostrar *\* dpy*, int *Screen*, int *\* attribList*)</span><span class="sxs-lookup"><span data-stu-id="57049-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="57049-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* ppfd*)</span><span class="sxs-lookup"><span data-stu-id="57049-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="57049-122">int **glXGetConfig**(display *\* dpy*, XVisualInfo *\* Vis*, int *\* attribList*, int *\* Value*)</span><span class="sxs-lookup"><span data-stu-id="57049-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="57049-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *ppfd*)</span><span class="sxs-lookup"><span data-stu-id="57049-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="57049-124">XVisualInfo \* **XGetVisualInfo**(display *\* dpy*, Long *vinfo \_ Mask*, XVisualInfo *\* vinfo \_ templ*, int *\* nitems*)</span><span class="sxs-lookup"><span data-stu-id="57049-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="57049-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="57049-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="57049-126">El *Visual* devuelto por **glxChooseVisual** se usa cuando se crea una ventana.</span><span class="sxs-lookup"><span data-stu-id="57049-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="57049-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* ppfd*)</span><span class="sxs-lookup"><span data-stu-id="57049-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="57049-128">En las secciones siguientes se proporcionan ejemplos de fragmentos de código de formato de píxel para un programa de sistema de ventana X y el mismo código después de que se haya trasladado a Windows.</span><span class="sxs-lookup"><span data-stu-id="57049-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="57049-129">GLX ejemplo de código de formato de píxeles</span><span class="sxs-lookup"><span data-stu-id="57049-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="57049-130">Ejemplo de código de formato de Windows píxeles</span><span class="sxs-lookup"><span data-stu-id="57049-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="57049-131">Para obtener más información sobre los formatos de píxeles, consulte [formatos de píxeles](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="57049-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




