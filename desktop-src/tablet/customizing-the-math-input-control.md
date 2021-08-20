---
description: Explica cómo cambiar la apariencia del control de entrada matemática.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personalización del Control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adedc4ab5b655f4f753a1b83cabe28e322adaad3c73bcf9f25ea1dea6d0bc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045636"
---
# <a name="customizing-the-math-input-control"></a>Personalización del Control de entrada matemática

Es posible cambiar la apariencia del control de entrada matemática para que sea más adecuado para la aplicación. En este tema se explican las distintas formas en que los desarrolladores pueden personalizar el control de entrada matemática.

Son posibles las siguientes personalizaciones:

-   [Cambiar los botones mostrados](#changing-the-displayed-buttons)
-   [Cambiar el título del control](#changing-the-control-caption)
-   [Cambiar el tamaño del área de vista previa del control](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Cambiar los botones mostrados

Puede cambiar los botones que se muestran en el control de entrada matemática para que el control tenga una funcionalidad extendida o aparezca más pequeño en la pantalla. Al habilitar el conjunto de botones extendido, se mostrarán los botones **Rehacer** **y Deshacer.** El código siguiente muestra cómo habilitar el conjunto de botones extendido.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



En la imagen siguiente se muestra el control con el conjunto extendido de botones.

![control de entrada matemática con un conjunto extendido de botones](images/mic.png)

En la imagen siguiente se muestra el control sin el conjunto extendido de botones.

![control de entrada matemática sin un conjunto extendido de botones](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Cambiar el título del control

Puede cambiar el título del control para el control de entrada matemática con el fin de establecer el título en la ventana del control de entrada matemática. El código siguiente muestra cómo establecer el título.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



En la imagen siguiente se muestra el control después de establecer el título.

![control de entrada matemática con un conjunto de subtítulos](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Cambiar el tamaño del área de vista previa del control

Puede personalizar el control de entrada matemática para que el control establezca explícitamente su tamaño de área de vista previa. Esto crea un área más grande en la que se muestran las fórmulas matemáticas. El código siguiente muestra cómo establecer el tamaño del área de vista previa.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



En las imágenes siguientes se muestra un control con áreas de vista previa de tamaño diferente.

![control de entrada matemática con el tamaño de área de vista previa predeterminado](images/mic.png)![control de entrada matemática con un área de vista previa mayor](images/mic-big-preview.png)

 

 



