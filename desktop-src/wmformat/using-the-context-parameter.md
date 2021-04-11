---
title: Usar el parámetro de contexto
description: Usar el parámetro de contexto
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- SDK de Windows Media Format, parámetro de contexto
- SDK de Windows Media Format, parámetro pvContext
- parámetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149074"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="e4ab3-106">Usar el parámetro de contexto</span><span class="sxs-lookup"><span data-stu-id="e4ab3-106">Using the Context Parameter</span></span>

<span data-ttu-id="e4ab3-107">Algunas de las devoluciones de llamada utilizadas por el SDK de Windows Media Format toman un parámetro denominado *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="e4ab3-108">Los objetos de llamada pasan a lo largo del valor especificado en el método que inició la acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="e4ab3-109">Por ejemplo, al llamar a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), puede pasar un valor para *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="e4ab3-110">Cuando el objeto de lector llama al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) para notificar a la aplicación que el archivo se ha abierto, pasará cualquier valor que se haya usado en la llamada a **Open** como el parámetro *pvContext* de en **status**.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="e4ab3-111">Este parámetro de contexto se proporciona para su uso y puede usarlo de la forma que desee.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="e4ab3-112">Normalmente, el parámetro *pvContext* se usa cuando es necesario que varios objetos compartan la misma devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="e4ab3-113">Por ejemplo, varios objetos usan el método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="e4ab3-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="e4ab3-114">Puede usar *pvContext* para permitir que los distintos objetos compartan una implementación de en **Estado** pasando un valor diferente para *pvContext* en la llamada original.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="e4ab3-115">En la implementación de en el **Estado**, puede crear una bifurcación de la lógica de control de mensajes basada en el valor de *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="e4ab3-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ab3-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4ab3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ab3-117">**Usar los métodos de devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="e4ab3-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




