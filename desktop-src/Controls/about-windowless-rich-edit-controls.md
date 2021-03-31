---
title: Acerca de los controles de edición enriquecida sin ventanas
description: Un control Rich Edit sin ventana, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un control Rich Edit sin proporcionar la ventana.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995649"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="5e051-103">Acerca de los controles de edición enriquecida sin ventanas</span><span class="sxs-lookup"><span data-stu-id="5e051-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="5e051-104">Un control Rich Edit sin ventana, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un [control Rich Edit](rich-edit-controls.md) sin proporcionar la ventana.</span><span class="sxs-lookup"><span data-stu-id="5e051-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="5e051-105">Para proporcionar la funcionalidad de una ventana, como la capacidad de recibir mensajes y un contexto de dispositivo en el que puede dibujar, los controles de edición enriquecida sin ventanas usan un par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="5e051-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="5e051-106">Para crear un control Rich Edit sin ventanas, llame a la función [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) con un puntero a la implementación de la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="5e051-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="5e051-107">**CreateTextServices** devuelve un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que puede consultar para recuperar un puntero a la implementación de [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) del control sin ventana.</span><span class="sxs-lookup"><span data-stu-id="5e051-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="5e051-108">Msftedit.dll exporta un identificador de interfaz (IID) denominado **IID \_ ITextServices** que puede usar para consultar el puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de la interfaz [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="5e051-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="5e051-109">En el ejemplo siguiente se muestra cómo recuperar el **IID \_ ITextServices** y usarlo para obtener la interfaz **ITextServices** .</span><span class="sxs-lookup"><span data-stu-id="5e051-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



<span data-ttu-id="5e051-110">Msftedit.dll también exporta un identificador de interfaz (IID) denominado **IID \_ ITextHost** que se puede usar de forma similar para consultar la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="5e051-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="5e051-111">La interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) tiene métodos a los que el control sin ventana llama para recuperar información sobre la ventana.</span><span class="sxs-lookup"><span data-stu-id="5e051-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="5e051-112">Por ejemplo, el objeto de servicios de texto llama al método [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) para recuperar un contexto de dispositivo en el que se puede dibujar.</span><span class="sxs-lookup"><span data-stu-id="5e051-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="5e051-113">El control sin ventana llama al método [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) para enviar notificaciones, como los mensajes de notificación de edición enriquecida, al host de texto.</span><span class="sxs-lookup"><span data-stu-id="5e051-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="5e051-114">El objeto servicios de texto llama a otros métodos **ITextHost** para solicitar al host de texto que realice otros servicios relacionados con la ventana.</span><span class="sxs-lookup"><span data-stu-id="5e051-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="5e051-115">Por ejemplo, el método [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) solicita al host de texto que agregue un rectángulo a la región de actualización de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5e051-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="5e051-116">Un control Rich Edit estándar tiene un procedimiento de ventana que procesa los mensajes del sistema y los mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e051-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="5e051-117">Puede usar el identificador de ventana del control para enviar mensajes de TI para realizar la edición de texto y otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="5e051-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="5e051-118">Pero un control Rich Edit sin ventanas no tiene ningún procedimiento de ventana para recibir y procesar mensajes.</span><span class="sxs-lookup"><span data-stu-id="5e051-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="5e051-119">En su lugar, proporciona una interfaz [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="5e051-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="5e051-120">Para enviar mensajes a un control Rich Edit sin ventanas, llame al método [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) .</span><span class="sxs-lookup"><span data-stu-id="5e051-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="5e051-121">Puede usar este método para enviar cualquiera de los mensajes Rich Edit o para pasar otros mensajes que afecten al control, como los mensajes del sistema para la entrada del mouse o del teclado.</span><span class="sxs-lookup"><span data-stu-id="5e051-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="5e051-122">También puede crear el objeto de servicios de texto como parte de un [objeto agregado por com](/windows/desktop/com/aggregation).</span><span class="sxs-lookup"><span data-stu-id="5e051-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="5e051-123">Esto hace que sea fácil agregar el objeto de servicios de texto con un objeto de modelo de objetos componentes (COM) sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="5e051-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 