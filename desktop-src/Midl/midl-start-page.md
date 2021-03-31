---
title: Lenguaje de definición de interfaz de Microsoft
description: El Lenguaje de definición de interfaz de Microsoft (MIDL) define las interfaces entre los programas de cliente y servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (vea Lenguaje de definición de interfaz de Microsoft MIDL)
- Lenguaje de definición de interfaz de Microsoft MIDL
- Lenguaje de definición de interfaz de Microsoft MIDL, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077649"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="7ccb2-107">Lenguaje de definición de interfaz de Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ccb2-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="7ccb2-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="7ccb2-108">Purpose</span></span>

<span data-ttu-id="7ccb2-109">El Lenguaje de definición de interfaz de Microsoft (MIDL) define las interfaces entre los programas de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="7ccb2-110">Microsoft incluye el compilador de MIDL con el kit de desarrollo de software (SDK) de la plataforma para que los desarrolladores puedan crear los archivos de lenguaje de definición de interfaz (IDL) y los archivos de configuración de la aplicación (ACF) necesarios para las interfaces de llamada a procedimiento remoto (RPC) y las interfaces COM/DCOM.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="7ccb2-111">MIDL también admite la generación de bibliotecas de tipos para la automatización OLE.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7ccb2-112">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="7ccb2-112">Where applicable</span></span>

<span data-ttu-id="7ccb2-113">Se puede usar MIDL en todas las aplicaciones cliente/servidor basadas en los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="7ccb2-114">También se puede usar para crear programas de cliente y servidor para entornos de red heterogéneos que incluyen sistemas operativos como UNIX y Apple.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="7ccb2-115">Microsoft admite el estándar DCE Open Group (anteriormente conocido como Open Software Foundation) para la interoperabilidad de RPC.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7ccb2-116">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="7ccb2-116">Developer audience</span></span>

<span data-ttu-id="7ccb2-117">Al usar MIDL con RPC, es necesario estar familiarizado con la programación de C/C++ y el paradigma de RPC.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="7ccb2-118">Al usar MIDL con COM, es necesario estar familiarizado con la programación de C++ y el paradigma de RPC a medida que se aplica a COM, o, como alternativa, estar familiarizado con el scripting de modelo de automatización OLE y las bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7ccb2-119">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7ccb2-119">Run-time requirements</span></span>

<span data-ttu-id="7ccb2-120">Las bibliotecas en tiempo de ejecución adecuadas para usar MIDL se incluyen con Windows.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="7ccb2-121">El compilador de MIDL y los componentes del entorno de desarrollo de RPC se instalan cuando se instala el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="7ccb2-122">Para obtener más información, vea [usar el compilador MIDL](using-the-midl-compiler-2.md) e [instalar el entorno de programación RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="7ccb2-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7ccb2-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7ccb2-123">In this section</span></span>



| <span data-ttu-id="7ccb2-124">Tema</span><span class="sxs-lookup"><span data-stu-id="7ccb2-124">Topic</span></span>                                                                                               | <span data-ttu-id="7ccb2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ccb2-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ccb2-126">Información general</span><span class="sxs-lookup"><span data-stu-id="7ccb2-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="7ccb2-127">Información general sobre MIDL y el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="7ccb2-128">Usar el compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="7ccb2-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="7ccb2-129">Información sobre el uso del compilador del de MIDL para generar código auxiliar de RPC.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="7ccb2-130">Definiciones de interfaz y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="7ccb2-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="7ccb2-131">Documentación de definiciones de interfaz y bibliotecas de tipos específicas de RPC.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="7ccb2-132">Referencia de Command-Line de MIDL</span><span class="sxs-lookup"><span data-stu-id="7ccb2-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="7ccb2-133">Documentación de los modificadores de la línea de comandos del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="7ccb2-134">Referencia del lenguaje MIDL</span><span class="sxs-lookup"><span data-stu-id="7ccb2-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="7ccb2-135">Referencia del lenguaje del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ccb2-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="7ccb2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ccb2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ccb2-137">Llamada a procedimiento remoto (RPC)</span><span class="sxs-lookup"><span data-stu-id="7ccb2-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

