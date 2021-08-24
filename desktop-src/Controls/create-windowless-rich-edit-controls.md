---
title: Cómo proporcionar controles rich edit sin ventana con funcionalidad de ventana
description: La funcionalidad de ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que se va a dibujar. Los controles de edición enriquecciones sin ventanas reciben esta funcionalidad mediante un par de interfaces ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698605"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Cómo proporcionar controles rich edit sin ventana con funcionalidad de ventana

La funcionalidad de ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que se va a dibujar. Los controles de edición enriquecciones sin ventanas reciben esta funcionalidad mediante un par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="establish-the-window-functionality"></a>Establecer la funcionalidad de ventana

En el código de ejemplo siguiente se muestra cómo crear el host de texto y los servicios de texto.


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>Comentarios

El *parámetro hmodRichEdit* del ejemplo de código es un identificador del módulo Msftedit.dll y se supone que este identificador ya se ha recuperado mediante una llamada a la función **GetModuleHandle.**

## <a name="complete-example"></a>Ejemplo completo

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit sin ventanas](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




