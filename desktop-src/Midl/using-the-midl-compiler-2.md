---
title: Usar el compilador MIDL
description: El compilador MIDL se instala automáticamente como parte del programa de instalación del kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas
- MIDL del compilador MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420663"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="b14c4-105">Usar el compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="b14c4-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="b14c4-106">El compilador MIDL se instala automáticamente como parte del programa de instalación del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="b14c4-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="b14c4-107">En los temas siguientes se describen los requisitos del compilador de MIDL C y del preprocesador de C, las bibliotecas de vínculos que forman parte del producto llamada a procedimiento remoto (RPC) y los archivos que genera MIDL para las interfaces DCOM, las interfaces RPC y las interfaces de la biblioteca de tipos de automatización OLE.</span><span class="sxs-lookup"><span data-stu-id="b14c4-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="b14c4-108">Invocar el compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="b14c4-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="b14c4-109">Archivos de respuesta</span><span class="sxs-lookup"><span data-stu-id="b14c4-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="b14c4-110">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="b14c4-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="b14c4-111">Consideraciones del compilador de C/C++</span><span class="sxs-lookup"><span data-stu-id="b14c4-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="b14c4-112">Usar la \_ \_ constante predefinida MIDL</span><span class="sxs-lookup"><span data-stu-id="b14c4-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="b14c4-113">MIDL y RPC</span><span class="sxs-lookup"><span data-stu-id="b14c4-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="b14c4-114">MIDL y COM</span><span class="sxs-lookup"><span data-stu-id="b14c4-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="b14c4-115">MIDL y ODL</span><span class="sxs-lookup"><span data-stu-id="b14c4-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="b14c4-116">Para obtener más información acerca de los archivos que componen el producto RPC, vea [instalar el entorno de programación RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="b14c4-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 