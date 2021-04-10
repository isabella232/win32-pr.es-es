---
title: Cómo proporcionar controles Rich Edit sin ventanas con funcionalidad de ventana
description: La funcionalidad de la ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que dibujar. Los controles de edición enriquecida sin ventanas reciben esta funcionalidad por medio de un par de interfaces ITextServices y ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103995041"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Cómo proporcionar controles Rich Edit sin ventanas con funcionalidad de ventana

La funcionalidad de la ventana incluye la capacidad de recibir mensajes y la propiedad de un contexto de dispositivo en el que dibujar. Los controles de edición enriquecida sin ventanas reciben esta funcionalidad por medio de un par de interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="establish-the-window-functionality"></a>Establecer la funcionalidad de la ventana

En el ejemplo de código siguiente se muestra cómo crear el host de texto y los servicios de texto.


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



## <a name="remarks"></a>Observaciones

El parámetro *hmodRichEdit* en el ejemplo de código es un identificador del módulo de Msftedit.dll y se supone que ya se ha recuperado este identificador mediante una llamada a la función **GetModuleHandle** .

## <a name="complete-example"></a>Ejemplo completo

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit sin ventanas](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




