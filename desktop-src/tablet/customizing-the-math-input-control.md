---
description: Explica cómo cambiar la apariencia del control de entrada matemática.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personalización del control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562965"
---
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="ec95b-103">Personalización del control de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="ec95b-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="ec95b-104">Es posible cambiar la apariencia y el funcionamiento del control de entrada matemática para que sea más adecuado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec95b-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="ec95b-105">En este tema se explican las distintas formas en que los desarrolladores pueden personalizar el control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="ec95b-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="ec95b-106">Se pueden realizar las siguientes personalizaciones:</span><span class="sxs-lookup"><span data-stu-id="ec95b-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="ec95b-107">Cambiar los botones mostrados</span><span class="sxs-lookup"><span data-stu-id="ec95b-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="ec95b-108">Cambiar el título del control</span><span class="sxs-lookup"><span data-stu-id="ec95b-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="ec95b-109">Cambiar el tamaño del área de vista previa del control</span><span class="sxs-lookup"><span data-stu-id="ec95b-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="ec95b-110">Cambiar los botones mostrados</span><span class="sxs-lookup"><span data-stu-id="ec95b-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="ec95b-111">Puede cambiar los botones que se muestran en el control de entrada matemática para que el control tenga funcionalidad ampliada o se muestre más pequeño en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ec95b-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="ec95b-112">Al habilitar el conjunto de botones extendidos se mostrarán los botones **rehacer** y **Deshacer** .</span><span class="sxs-lookup"><span data-stu-id="ec95b-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="ec95b-113">En el código siguiente se muestra cómo habilitar el conjunto de botones extendido.</span><span class="sxs-lookup"><span data-stu-id="ec95b-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="ec95b-114">En la imagen siguiente se muestra el control con el conjunto extendido de botones.</span><span class="sxs-lookup"><span data-stu-id="ec95b-114">The following image shows the control with the extended set of buttons.</span></span>

![control de entrada matemática con un conjunto extendido de botones](images/mic.png)

<span data-ttu-id="ec95b-116">En la imagen siguiente se muestra el control sin el conjunto extendido de botones.</span><span class="sxs-lookup"><span data-stu-id="ec95b-116">The following image shows the control without the extended set of buttons.</span></span>

![control de entrada matemática sin un conjunto extendido de botones](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="ec95b-118">Cambiar el título del control</span><span class="sxs-lookup"><span data-stu-id="ec95b-118">Changing the Control Caption</span></span>

<span data-ttu-id="ec95b-119">Puede cambiar el título del control para el control de entrada matemática para establecer el título en la ventana del control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="ec95b-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="ec95b-120">En el código siguiente se muestra cómo establecer el título.</span><span class="sxs-lookup"><span data-stu-id="ec95b-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="ec95b-121">La siguiente imagen muestra el control una vez establecido el título.</span><span class="sxs-lookup"><span data-stu-id="ec95b-121">The following image shows the control after the caption has been set.</span></span>

![control de entrada matemática con un conjunto de leyendas](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="ec95b-123">Cambiar el tamaño del área de vista previa del control</span><span class="sxs-lookup"><span data-stu-id="ec95b-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="ec95b-124">Puede personalizar el control de entrada matemática para que el control establezca explícitamente su tamaño de área de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ec95b-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="ec95b-125">Esto crea un área más grande en la que se muestran las fórmulas matemáticas.</span><span class="sxs-lookup"><span data-stu-id="ec95b-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="ec95b-126">En el código siguiente se muestra cómo establecer el tamaño del área de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ec95b-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="ec95b-127">En las imágenes siguientes se muestra un control con áreas de vista previa de diferentes tamaños.</span><span class="sxs-lookup"><span data-stu-id="ec95b-127">The following images show a control with differently sized preview areas.</span></span>

![control de entrada matemática con el tamaño de área de vista previa predeterminada](images/mic.png)![control de entrada matemática con un área de vista previa más grande](images/mic-big-preview.png)

 

 



