---
title: Preparación de la aplicación para Windows de 64 bits
description: Hay varias características que facilitan el desarrollo de aplicaciones que se ejecutarán en Windows de 32 y 64 bits. La mayoría de ellos, como los nuevos tipos de datos, se describen en preparar para Windows de 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Kit de herramientas de 64 bits de la programación para Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271349"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="5835e-105">Preparación de la aplicación para Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="5835e-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="5835e-106">Hay varias características que facilitan el desarrollo de aplicaciones que se ejecutarán en Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5835e-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="5835e-107">La mayoría de ellos, como los nuevos tipos de datos, se describen en [preparar para Windows de 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="5835e-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="5835e-108">El kit de herramientas de 64 bits incluido con el Windows SDK incluye un compilador de MIDL de 64 bits, Midl.exe, para generar código auxiliar de 64 bits nativo, así como códigos auxiliares de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5835e-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="5835e-109">Use el conmutador **/env Win64** para generar solo códigos auxiliares de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5835e-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="5835e-110">El valor predeterminado es generar código auxiliar dual que se ejecute en ambas plataformas.</span><span class="sxs-lookup"><span data-stu-id="5835e-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="5835e-111">Tenga en cuenta que el MIDL de 64 bits solo admite los modos de optimización [**/Oicf**](/windows/desktop/Midl/-oi) y [**/os**](/windows/desktop/Midl/-os) .</span><span class="sxs-lookup"><span data-stu-id="5835e-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 