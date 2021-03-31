---
title: Trasladar contextos de representación
description: Trasladar contextos de representación
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextos de representación OpenGL, Porting
- OpenGL en Windows, contextos de representación
- trasladar a OpenGL, contextos de representación
- Portabilidad de OpenGL, contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418874"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="1e7b7-107">Trasladar contextos de representación</span><span class="sxs-lookup"><span data-stu-id="1e7b7-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="1e7b7-108">El sistema de ventanas X y las ventanas se representan a través de contextos de representación.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="1e7b7-109">Seis funciones GLX administrar contextos de representación y cinco de ellos tienen una función de Windows equivalente.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="1e7b7-110">En la tabla siguiente se enumeran las funciones de representación de GLX y sus funciones de Windows equivalentes.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="1e7b7-111">Función de contexto de representación GLX</span><span class="sxs-lookup"><span data-stu-id="1e7b7-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="1e7b7-112">Función de contexto de representación de Windows</span><span class="sxs-lookup"><span data-stu-id="1e7b7-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="1e7b7-113">GLXContext **glXCopyContext**(display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="1e7b7-114">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="1e7b7-115">GLXContext **glXCreateContext**(display *\* dpy*, XVisualInfo *\* Vis*, GLXContext *shareList*, bool *Direct*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="1e7b7-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="1e7b7-117">void **glXDeleteContext**(display *\* dpy*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="1e7b7-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="1e7b7-119">GLXContext **glXGetCurrentContext**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="1e7b7-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="1e7b7-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="1e7b7-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="1e7b7-123">Bool **glXMakeCurrent**(display *\* dpy*, GLXDrawable *Draw*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="1e7b7-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="1e7b7-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="1e7b7-125">Los tipos de valor devuelto y otros tipos tienen nombres diferentes en el sistema de ventana X que en Windows.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="1e7b7-126">Puede buscar apariciones de GLXContext para ayudar a encontrar partes del código que deben migrarse.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="1e7b7-127">En las secciones siguientes se comparan los ejemplos de código de contexto de representación en un programa de sistema X Window y el mismo código después de que se haya trasladado a Windows.</span><span class="sxs-lookup"><span data-stu-id="1e7b7-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="1e7b7-128">Para obtener más información sobre la representación de contextos, vea [contextos de representación](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="1e7b7-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




