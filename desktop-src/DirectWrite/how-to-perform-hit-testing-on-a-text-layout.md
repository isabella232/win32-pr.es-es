---
title: Cómo realizar pruebas de posicionamiento en un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar pruebas de posicionamiento a una aplicación de DirectWrite que muestre texto mediante la interfaz IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003448"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="90f4c-103">Cómo realizar pruebas de posicionamiento en un diseño de texto</span><span class="sxs-lookup"><span data-stu-id="90f4c-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="90f4c-104">Proporciona un breve tutorial sobre cómo agregar pruebas de posicionamiento a una aplicación de [DirectWrite](direct-write-portal.md) que muestre texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="90f4c-105">El resultado de este tutorial es una aplicación que subraya el carácter en el que se hace clic con el botón primario del mouse, tal como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="90f4c-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![captura de pantalla de "haga clic en este texto"](images/hittest.png)

<span data-ttu-id="90f4c-107">Esto contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="90f4c-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="90f4c-108">Paso 1: crear un diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="90f4c-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="90f4c-109">Paso 2: agregar un método OnClick.</span><span class="sxs-lookup"><span data-stu-id="90f4c-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="90f4c-110">Paso 3: realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="90f4c-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="90f4c-111">Paso 4: subrayar el texto en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="90f4c-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="90f4c-112">Paso 5: controlar el mensaje de LBUTTONDOWN de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="90f4c-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="90f4c-113">Paso 1: crear un diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="90f4c-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="90f4c-114">Para empezar, necesitará una aplicación que use un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="90f4c-115">Si ya tiene una aplicación que muestra texto con un diseño de texto, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="90f4c-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="90f4c-116">Para agregar un diseño de texto, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="90f4c-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="90f4c-117">Declare un puntero a una interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase.</span><span class="sxs-lookup"><span data-stu-id="90f4c-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="90f4c-118">Al final del método **CreateDeviceIndependentResources** , cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

    ```cpp
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    ```

3. <span data-ttu-id="90f4c-119">A continuación, debe cambiar la llamada al método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) a [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="90f4c-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="90f4c-120">Paso 2: agregar un método OnClick.</span><span class="sxs-lookup"><span data-stu-id="90f4c-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="90f4c-121">Ahora, agregue un método a la clase que usará la funcionalidad de prueba de posicionamiento del diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="90f4c-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="90f4c-122">Declare un método **onclick** en el archivo de encabezado de clase.</span><span class="sxs-lookup"><span data-stu-id="90f4c-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="90f4c-123">Defina un método **onclick** en el archivo de implementación de clase.</span><span class="sxs-lookup"><span data-stu-id="90f4c-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="90f4c-124">Paso 3: realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="90f4c-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="90f4c-125">Para determinar dónde ha haga clic el usuario en el diseño de texto, usaremos el método [**IDWriteTextLayout:: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="90f4c-126">Agregue lo siguiente al método **onclick** que definió en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="90f4c-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="90f4c-127">Declare las variables que se van a pasar como parámetros al método.</span><span class="sxs-lookup"><span data-stu-id="90f4c-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="90f4c-128">El método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) genera los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="90f4c-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="90f4c-129">Variable</span><span class="sxs-lookup"><span data-stu-id="90f4c-129">Variable</span></span>         | <span data-ttu-id="90f4c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="90f4c-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="90f4c-131">*hitTestMetrics*</span><span class="sxs-lookup"><span data-stu-id="90f4c-131">*hitTestMetrics*</span></span> | <span data-ttu-id="90f4c-132">Geometría que incluye completamente la ubicación de la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="90f4c-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="90f4c-133">*isInside*</span><span class="sxs-lookup"><span data-stu-id="90f4c-133">*isInside*</span></span>       | <span data-ttu-id="90f4c-134">Indica si la ubicación de la prueba de posicionamiento está dentro de la cadena de texto o no.</span><span class="sxs-lookup"><span data-stu-id="90f4c-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="90f4c-135">Cuando es FALSE, se devuelve la posición más cercana al borde del texto.</span><span class="sxs-lookup"><span data-stu-id="90f4c-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="90f4c-136">*isTrailingHit*</span><span class="sxs-lookup"><span data-stu-id="90f4c-136">*isTrailingHit*</span></span>  | <span data-ttu-id="90f4c-137">Indica si la ubicación de la prueba de posicionamiento está en el lado inicial o final del carácter.</span><span class="sxs-lookup"><span data-stu-id="90f4c-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="90f4c-138">Llame al método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) del objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="90f4c-139">El código de este ejemplo pasa las  variables x *e y de* la posición sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="90f4c-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="90f4c-140">Esto puede hacerse en este ejemplo porque el diseño del texto tiene el mismo tamaño que la ventana y se origina en la esquina superior izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="90f4c-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="90f4c-141">Si no fuera así, tendría que determinar las coordenadas en relación con el origen del diseño del texto.</span><span class="sxs-lookup"><span data-stu-id="90f4c-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="90f4c-142">Paso 4: subrayar el texto en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="90f4c-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="90f4c-143">Agregue lo siguiente al **onclick** que definió en el paso 2, después de la llamada al método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="90f4c-144">Este código hace lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="90f4c-144">This code does the following.</span></span>

1. <span data-ttu-id="90f4c-145">Comprueba si el punto de prueba de aciertos estaba dentro del texto mediante la variable *isInside* .</span><span class="sxs-lookup"><span data-stu-id="90f4c-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="90f4c-146">El miembro **textPosition** de la estructura *hitTestMetrics* contiene el índice de base cero del carácter en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="90f4c-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="90f4c-147">Obtiene el subrayado de este carácter pasando este valor al método [**IDWriteTextLayout:: GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="90f4c-148">Declara una variable [**de \_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) con la posición de inicio establecida en **hitTestMetrics. textPosition** y una longitud de 1.</span><span class="sxs-lookup"><span data-stu-id="90f4c-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="90f4c-149">Alterna el subrayado mediante el método [**IDWriteTextLayout:: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="90f4c-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="90f4c-150">Después de establecer el subrayado, vuelva a dibujar el texto llamando al método **DrawD2DContent** de la clase.</span><span class="sxs-lookup"><span data-stu-id="90f4c-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="90f4c-151">Paso 5: controlar el mensaje de LBUTTONDOWN de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="90f4c-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="90f4c-152">Por último, agregue el mensaje de **\_ LBUTTONDOWN de WM** al controlador de mensajes de la aplicación y llame al método **onclick** de la clase.</span><span class="sxs-lookup"><span data-stu-id="90f4c-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="90f4c-153">**Obtener \_ Las macros x \_ lParam** y **Get \_ X \_ lParam** se declaran en el archivo de encabezado windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="90f4c-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="90f4c-154">Recuperan fácilmente la posición x e y del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="90f4c-154">They easily retrieve the x and y position of the mouse click.</span></span>
