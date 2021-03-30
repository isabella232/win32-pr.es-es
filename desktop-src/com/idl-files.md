---
title: Archivos IDL
description: Archivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904848"
---
# <a name="idl-files"></a><span data-ttu-id="c3ffa-103">Archivos IDL</span><span class="sxs-lookup"><span data-stu-id="c3ffa-103">IDL Files</span></span>

<span data-ttu-id="c3ffa-104">COM utiliza el Lenguaje de definición de interfaz de Microsoft (MIDL) para describir objetos COM.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="c3ffa-105">MIDL es una extensión de IDL para entornos de computación distribuida definidos por Open Software Foundation, desarrollado para definir interfaces para llamadas a procedimientos remotos en aplicaciones cliente/servidor tradicionales.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="c3ffa-106">MIDL incluye la mayoría de los atributos y las instrucciones del lenguaje de definición de objetos (ODL), el lenguaje que se usó originalmente para generar bibliotecas de tipos para la automatización OLE.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="c3ffa-107">En C++ y Java, un desarrollador que crea un objeto COM crea un archivo IDL que el compilador MIDL procesa para crear una biblioteca de tipos o archivos de encabezado y proxy, o ambos.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="c3ffa-108">Una *biblioteca de tipos* es un archivo binario que describe el objeto com o las interfaces com, o ambos.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="c3ffa-109">Una biblioteca de tipos es la versión compilada del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="c3ffa-110">Sin embargo, las bibliotecas de tipos solo admiten la semántica de ODL.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="c3ffa-111">En concreto, no pueden representar toda la información de un archivo IDL relacionado con atributos IDL como \[ [**el tamaño \_ es**](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="c3ffa-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="c3ffa-112">Debe crear y usar archivos proxy para los archivos IDL afectados por la pérdida de información en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="c3ffa-113">En Visual Basic, un desarrollador que crea un objeto COM no crea un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="c3ffa-114">En su lugar, Visual Basic recopila información mediante las propiedades de clase y proyecto y crea directamente la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c3ffa-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 