---
title: Usar la devolución de llamada en estado
description: Usar la devolución de llamada en estado
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- SDK de Windows Media Format, método de devolución de llamada de estado
- SDK de Windows Media Format, interfaz IWMStatusCallback
- Método de devolución de llamada de estado, acerca de
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994926"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="d3c7c-107">Usar la devolución de llamada en estado</span><span class="sxs-lookup"><span data-stu-id="d3c7c-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="d3c7c-108">Varios objetos del SDK de formato de Windows Media llaman al método de devolución de llamada [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) OnFormat.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="d3c7c-109">En **Estado** recibe mensajes que representan cambios en el estado de las operaciones del SDK.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="d3c7c-110">Para usar el método de devolución de llamada en **Estado** , debe implementar una clase en la aplicación que herede de la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) .</span><span class="sxs-lookup"><span data-stu-id="d3c7c-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="d3c7c-111">Incluya código para su versión de en **Estado** en la clase.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="d3c7c-112">En los ejemplos incluidos con este SDK se pueden encontrar varios ejemplos de implementaciones de **Estado** .</span><span class="sxs-lookup"><span data-stu-id="d3c7c-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="d3c7c-113">Para obtener más información acerca de los ejemplos, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d3c7c-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="d3c7c-114">Debe asociar la implementación de la devolución de llamada de estado con varios objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="d3c7c-115">Cada objeto tiene una forma diferente de crear esta asociación.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="d3c7c-116">Para obtener una lista de los métodos que asocian objetos específicos, vea la página de referencia de **IWMStatusCallback** .</span><span class="sxs-lookup"><span data-stu-id="d3c7c-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="d3c7c-117">Los mensajes de estado que se pueden recibir en **Estado** se definen en el tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="d3c7c-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="d3c7c-118">Puede elegir qué mensajes desea interceptar y qué omitir.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="d3c7c-119">Sin embargo, es necesario responder a algunos mensajes de estado para determinadas características.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="d3c7c-120">Por ejemplo, al usar el lector asincrónico, el método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) abre un archivo de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="d3c7c-121">La única forma de saber cuándo se ha abierto el archivo es atrapar el \_ mensaje abierto de MWT.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="d3c7c-122">Normalmente, los mensajes a los que responde son notificaciones de la finalización de las tareas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="d3c7c-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c7c-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3c7c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c7c-124">**Usar los métodos de devolución de llamada**</span><span class="sxs-lookup"><span data-stu-id="d3c7c-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




