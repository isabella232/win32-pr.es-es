---
description: En Microsoft Media Foundation, una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Colas de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277070"
---
# <a name="work-queues"></a><span data-ttu-id="7a260-103">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="7a260-103">Work Queues</span></span>

<span data-ttu-id="7a260-104">En Microsoft Media Foundation, una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="7a260-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="7a260-105">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7a260-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a260-106">Tema</span><span class="sxs-lookup"><span data-stu-id="7a260-106">Topic</span></span></th>
<th><span data-ttu-id="7a260-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a260-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a260-108"><a href="using-work-queues.md">Uso de colas de trabajo</a></span><span class="sxs-lookup"><span data-stu-id="7a260-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="7a260-109">Describe cómo una aplicación o un componente puede usar colas de trabajo para realizar operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="7a260-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a260-110"><a href="writing-an-asynchronous-method.md">Escribir un método asincrónico</a></span><span class="sxs-lookup"><span data-stu-id="7a260-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="7a260-111">Describe cómo escribir un método asincrónico que sigue el patrón Begin/end descrito en métodos de <a href="asynchronous-callback-methods.md">devolución de llamada asincrónica</a>.</span><span class="sxs-lookup"><span data-stu-id="7a260-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a260-112"><a href="custom-asynchronous-result-objects.md">Objetos de resultado asincrónicos personalizados</a></span><span class="sxs-lookup"><span data-stu-id="7a260-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="7a260-113">Describe cómo crear una implementación personalizada de la interfaz <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7a260-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7a260-114">La mayoría de las aplicaciones deben usar la implementación estándar que proporciona <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7a260-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="7a260-115">Este tema está destinado a aplicaciones con requisitos avanzados.</span><span class="sxs-lookup"><span data-stu-id="7a260-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a260-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Mejoras en la cola de trabajo y subprocesos</a></span><span class="sxs-lookup"><span data-stu-id="7a260-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="7a260-117">Describe las mejoras en Windows 8 para los subprocesos y las colas de trabajo en la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7a260-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7a260-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a260-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a260-119">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="7a260-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




