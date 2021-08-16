---
title: Cómo usar métodos tab en TOM
description: En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en Text Object Model (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b4a101c2deb3c22993f41b11ee94df6ac738da41963046f02a072f3eaa6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828617"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Cómo usar métodos tab en TOM

En el ejemplo siguiente se proporcionan funciones de C que ilustran el uso de los métodos de tabulación en Text Object Model (TOM). Se supone que la mayoría de las aplicaciones incluyen una barra de herramientas que muestra la posición actual y el tipo de las pestañas del párrafo seleccionado actualmente.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-tab-method"></a>Usar un método Tab

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



### <a name="copy-tab-information"></a>Copiar información de pestaña

En el ejemplo siguiente se muestra cómo copiar solo la información de tabulación de una [**interfaz ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a otra. Toma dos parámetros: **ITextPara** pParaFrom (el párrafo desde el que se copian las \*  pestañas) e **ITextPara** \* *pParaFrom* (el párrafo en el que se copian las pestañas).


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

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




