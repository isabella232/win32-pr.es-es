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
# <a name="about-windowless-rich-edit-controls"></a>Acerca de los controles de edición enriquecida sin ventanas

Un control Rich Edit sin ventana, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un [control Rich Edit](rich-edit-controls.md) sin proporcionar la ventana. Para proporcionar la funcionalidad de una ventana, como la capacidad de recibir mensajes y un contexto de dispositivo en el que puede dibujar, los controles de edición enriquecida sin ventanas usan un par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Para crear un control Rich Edit sin ventanas, llame a la función [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) con un puntero a la implementación de la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) . **CreateTextServices** devuelve un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que puede consultar para recuperar un puntero a la implementación de [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) del control sin ventana.

Msftedit.dll exporta un identificador de interfaz (IID) denominado **IID \_ ITextServices** que puede usar para consultar el puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de la interfaz [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . En el ejemplo siguiente se muestra cómo recuperar el **IID \_ ITextServices** y usarlo para obtener la interfaz **ITextServices** .


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



Msftedit.dll también exporta un identificador de interfaz (IID) denominado **IID \_ ITextHost** que se puede usar de forma similar para consultar la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .

La interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) tiene métodos a los que el control sin ventana llama para recuperar información sobre la ventana. Por ejemplo, el objeto de servicios de texto llama al método [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) para recuperar un contexto de dispositivo en el que se puede dibujar. El control sin ventana llama al método [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) para enviar notificaciones, como los mensajes de notificación de edición enriquecida, al host de texto. El objeto servicios de texto llama a otros métodos **ITextHost** para solicitar al host de texto que realice otros servicios relacionados con la ventana. Por ejemplo, el método [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) solicita al host de texto que agregue un rectángulo a la región de actualización de la ventana.

Un control Rich Edit estándar tiene un procedimiento de ventana que procesa los mensajes del sistema y los mensajes de la aplicación. Puede usar el identificador de ventana del control para enviar mensajes de TI para realizar la edición de texto y otras operaciones. Pero un control Rich Edit sin ventanas no tiene ningún procedimiento de ventana para recibir y procesar mensajes. En su lugar, proporciona una interfaz [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Para enviar mensajes a un control Rich Edit sin ventanas, llame al método [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) . Puede usar este método para enviar cualquiera de los mensajes Rich Edit o para pasar otros mensajes que afecten al control, como los mensajes del sistema para la entrada del mouse o del teclado.

También puede crear el objeto de servicios de texto como parte de un [objeto agregado por com](/windows/desktop/com/aggregation). Esto hace que sea fácil agregar el objeto de servicios de texto con un objeto de modelo de objetos componentes (COM) sin ventanas.

 

 