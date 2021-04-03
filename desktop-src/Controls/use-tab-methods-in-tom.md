---
title: Cómo usar métodos de ficha en TOM
description: En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en el modelo de objetos de texto (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904456"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Cómo usar métodos de ficha en TOM

En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en el modelo de objetos de texto (TOM). Se supone que la mayoría de las aplicaciones incluyen una barra de herramientas que muestra la posición actual y el tipo de las pestañas del párrafo seleccionado actualmente.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-a-tab-method"></a>Usar un método de tabulación

En el ejemplo de código siguiente se muestra cómo actualizar una barra de herramientas con los detalles de la pestaña actual.


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a>Copiar información de pestañas

En el ejemplo siguiente se muestra cómo copiar solo la información de la pestaña de una interfaz [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a otra. Toma dos parámetros: **ITextPara** \* *pParaFrom* (el párrafo del que se copian las pestañas) y **ITextPara** \* *pParaFrom* (el párrafo en el que se copian las pestañas).


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modelo de objetos de texto](using-the-text-object-model.md)
</dt> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




