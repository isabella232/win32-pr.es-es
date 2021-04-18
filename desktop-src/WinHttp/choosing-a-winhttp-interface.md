---
description: Antes de empezar a desarrollar una aplicación de servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si va a usar la API de C/C++ o la interfaz COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Elección de una interfaz WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716221"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="c866b-103">Elección de una interfaz WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c866b-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="c866b-104">Antes de empezar a desarrollar una aplicación de servicios HTTP de Microsoft Windows (WinHTTP), primero debe decidir si va a usar la API de C/C++ o la interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="c866b-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="c866b-105">En la tabla siguiente se resumen las ventajas y desventajas asociadas a cada uno de estos enfoques.</span><span class="sxs-lookup"><span data-stu-id="c866b-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c866b-106">API DE C/C++</span><span class="sxs-lookup"><span data-stu-id="c866b-106">C/C++ API</span></span></th>
<th><span data-ttu-id="c866b-107">Interfaz COM</span><span class="sxs-lookup"><span data-stu-id="c866b-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c866b-108">Ventajas</span><span class="sxs-lookup"><span data-stu-id="c866b-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="c866b-109">Las respuestas se pueden procesar en fragmentos, lo que es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="c866b-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="c866b-110">Las operaciones POST también se pueden procesar en fragmentos y acelerar el tiempo de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="c866b-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="c866b-111">Compatibilidad con AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="c866b-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="c866b-112">Acceso al conjunto completo de características de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c866b-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="c866b-113">Los datos binarios se pueden controlar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="c866b-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c866b-114">Crear una aplicación es fácil y requiere menos líneas de código que la API de C/C++.</span><span class="sxs-lookup"><span data-stu-id="c866b-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="c866b-115">La interfaz se puede usar en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="c866b-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c866b-116">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="c866b-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="c866b-117">El procesamiento es más complejo.</span><span class="sxs-lookup"><span data-stu-id="c866b-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="c866b-118">La API de C/C++ requiere más pasos que la interfaz COM para realizar las mismas acciones.</span><span class="sxs-lookup"><span data-stu-id="c866b-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="c866b-119">La configuración de una solicitud requiere más código.</span><span class="sxs-lookup"><span data-stu-id="c866b-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c866b-120">La interfaz COM no proporciona acceso al conjunto completo de características de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c866b-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="c866b-121">Es difícil administrar los tipos de datos binarios en algunos lenguajes de scripting, como VBScript y JScript.</span><span class="sxs-lookup"><span data-stu-id="c866b-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="c866b-122">La interfaz COM no es compatible con el proxy de.</span><span class="sxs-lookup"><span data-stu-id="c866b-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="c866b-123">Las aplicaciones deben utilizar el modelo de APARTMENT_THREADED COM.</span><span class="sxs-lookup"><span data-stu-id="c866b-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="c866b-124">Antes de que se pueda empezar a procesar una respuesta, primero se debe recibir y almacenar en búfer la respuesta completa.</span><span class="sxs-lookup"><span data-stu-id="c866b-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



