---
title: Fuentes de colores
description: En este tema se describen las fuentes de color, su compatibilidad en DirectWrite y Direct2D, y cómo utilizarlas en la aplicación.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104557795"
---
# <a name="color-fonts"></a><span data-ttu-id="a9d58-103">Fuentes de colores</span><span class="sxs-lookup"><span data-stu-id="a9d58-103">Color Fonts</span></span>

<span data-ttu-id="a9d58-104">En este tema se describen las fuentes de color, su compatibilidad en DirectWrite y Direct2D, y cómo utilizarlas en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9d58-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="a9d58-105">Este documento contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="a9d58-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="a9d58-106">¿Qué son las fuentes de color?</span><span class="sxs-lookup"><span data-stu-id="a9d58-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="a9d58-107">¿Por qué usar fuentes de color?</span><span class="sxs-lookup"><span data-stu-id="a9d58-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="a9d58-108">¿Qué tipos de fuentes de color admite Windows?</span><span class="sxs-lookup"><span data-stu-id="a9d58-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="a9d58-109">Usar fuentes de color</span><span class="sxs-lookup"><span data-stu-id="a9d58-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="a9d58-110">Usar fuentes de color en una aplicación XAML</span><span class="sxs-lookup"><span data-stu-id="a9d58-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="a9d58-111">Usar fuentes de color en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a9d58-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="a9d58-112">Usar fuentes de color con DirectWrite y Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9d58-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="a9d58-113">Usar fuentes de color con Win2D</span><span class="sxs-lookup"><span data-stu-id="a9d58-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="a9d58-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9d58-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="a9d58-115">¿Qué son las fuentes de color?</span><span class="sxs-lookup"><span data-stu-id="a9d58-115">What are color fonts?</span></span>

<span data-ttu-id="a9d58-116">Las fuentes de color, también conocidas como fuentes multicolores o fuentes cromáticas, son una tecnología de fuentes que permite a los diseñadores de fuentes usar varios colores dentro de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="a9d58-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="a9d58-117">Las fuentes de color permiten escenarios de texto multicolor en aplicaciones y sitios web con menos código y una compatibilidad de sistema operativo más sólida que las técnicas ad hoc implementadas por encima del sistema de representación de texto.</span><span class="sxs-lookup"><span data-stu-id="a9d58-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="a9d58-118">Las fuentes con las que probablemente esté familiarizado no son fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="a9d58-119">Estas fuentes definen solo la forma de los glifos que contienen, ya sea con contornos vectoriales o con mapas de bits monocromáticos.</span><span class="sxs-lookup"><span data-stu-id="a9d58-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="a9d58-120">En el momento de dibujar, un representador de texto rellena la forma de glifo usando un color único (el color de fuente) especificado por la aplicación o el documento que se está representando.</span><span class="sxs-lookup"><span data-stu-id="a9d58-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="a9d58-121">Por otro lado, las fuentes de color contienen información de color además de la información de forma.</span><span class="sxs-lookup"><span data-stu-id="a9d58-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="a9d58-122">Algunos enfoques permiten a los diseñadores de fuentes ofrecer varias paletas de colores, lo que proporciona la flexibilidad artística de fuente de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="a9d58-123">En el ejemplo siguiente se muestra un glifo de la fuente de color Segoe UI Emoji.</span><span class="sxs-lookup"><span data-stu-id="a9d58-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="a9d58-124">El glifo se representa en monocromo a la izquierda y en color a la derecha.</span><span class="sxs-lookup"><span data-stu-id="a9d58-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Muestra glifos en paralelo, el glifo izquierdo representado en monocromo, el derecho en la fuente de color Segoe U I Emoji.](images/color-font-cat.png)

<span data-ttu-id="a9d58-126">Las fuentes de color suelen incluir información de reserva para plataformas que no admiten fuentes de color o para escenarios en los que se ha deshabilitado la funcionalidad de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="a9d58-127">En esas plataformas, las fuentes de color se representan como fuentes monocromáticas normales.</span><span class="sxs-lookup"><span data-stu-id="a9d58-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="a9d58-128">¿Por qué usar fuentes de color?</span><span class="sxs-lookup"><span data-stu-id="a9d58-128">Why use color fonts?</span></span>

<span data-ttu-id="a9d58-129">Históricamente, los diseñadores y desarrolladores han usado diversas técnicas para lograr el texto multicolor.</span><span class="sxs-lookup"><span data-stu-id="a9d58-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="a9d58-130">Por ejemplo, los sitios web suelen usar imágenes de tramas en lugar de texto para mostrar encabezados completos.</span><span class="sxs-lookup"><span data-stu-id="a9d58-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="a9d58-131">Este enfoque permite una flexibilidad artística, pero los gráficos de tramas no se adaptan bien a todos los tamaños de pantalla, ni proporcionan las mismas características de accesibilidad que el texto real.</span><span class="sxs-lookup"><span data-stu-id="a9d58-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="a9d58-132">Otra técnica común es superponer varias fuentes monocromáticas en diferentes colores de fuente, pero esto normalmente requiere un código de diseño adicional para administrar.</span><span class="sxs-lookup"><span data-stu-id="a9d58-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="a9d58-133">Las fuentes de color ofrecen una manera de lograr estos efectos visuales con toda la simplicidad y funcionalidad de las fuentes normales.</span><span class="sxs-lookup"><span data-stu-id="a9d58-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="a9d58-134">El texto representado en una fuente de color es el mismo que el de otro texto: puede copiarse y pegarse, puede ser analizado por herramientas de accesibilidad, etc.</span><span class="sxs-lookup"><span data-stu-id="a9d58-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="a9d58-135">¿Qué tipos de fuentes de color admite Windows?</span><span class="sxs-lookup"><span data-stu-id="a9d58-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="a9d58-136">La [especificación OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) define varias maneras de insertar información de color en una fuente.</span><span class="sxs-lookup"><span data-stu-id="a9d58-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="a9d58-137">A partir de la actualización de aniversario de Windows 10, DirectWrite y Direct2D (y los marcos de trabajo de Windows integrados) admiten todos estos enfoques.</span><span class="sxs-lookup"><span data-stu-id="a9d58-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="a9d58-138">Se resumen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="a9d58-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="a9d58-139">Técnica</span><span class="sxs-lookup"><span data-stu-id="a9d58-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="a9d58-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9d58-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d58-141">[COLR](/typography/opentype/spec/colr) / Tablas de [CPAL](/typography/opentype/spec/cpal)</span><span class="sxs-lookup"><span data-stu-id="a9d58-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="a9d58-142">Utiliza capas de vectores de color, cuyas formas se definen de la misma manera que los contornos de glifo de un solo color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="a9d58-143">**Nota:** Se admite a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a9d58-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="a9d58-144">Tabla [SVG](/typography/opentype/spec/svg)</span><span class="sxs-lookup"><span data-stu-id="a9d58-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="a9d58-145">Utiliza imágenes vectoriales creadas en el formato de gráficos vectoriales escalables.</span><span class="sxs-lookup"><span data-stu-id="a9d58-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="a9d58-146">**Nota:** A partir de la actualización de aniversario de Windows 10, DirectWrite admite un subconjunto de la especificación SVG completa. No se garantiza que todo el contenido SVG se represente en una fuente SVG OpenType.</span><span class="sxs-lookup"><span data-stu-id="a9d58-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="a9d58-147">Consulte [compatibilidad con SVG](../direct2d/svg-support.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="a9d58-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="a9d58-148">[CBDT](/typography/opentype/spec/cbdt) / Tablas de [CBLC](/typography/opentype/spec/cblc)</span><span class="sxs-lookup"><span data-stu-id="a9d58-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="a9d58-149">Utiliza imágenes de mapa de bits de color incrustado.</span><span class="sxs-lookup"><span data-stu-id="a9d58-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a9d58-150">tabla [sbix](/typography/opentype/spec/sbix)</span><span class="sxs-lookup"><span data-stu-id="a9d58-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="a9d58-151">Utiliza imágenes de mapa de bits de color incrustado.</span><span class="sxs-lookup"><span data-stu-id="a9d58-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="a9d58-152">Usar fuentes de color</span><span class="sxs-lookup"><span data-stu-id="a9d58-152">Using color fonts</span></span>

<span data-ttu-id="a9d58-153">Desde la perspectiva del usuario, las fuentes de color son simplemente fuentes.</span><span class="sxs-lookup"><span data-stu-id="a9d58-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="a9d58-154">Por ejemplo, normalmente se pueden instalar y desinstalar del sistema de la misma manera que las fuentes monocromáticas, y se representan como texto normal y seleccionable.</span><span class="sxs-lookup"><span data-stu-id="a9d58-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="a9d58-155">También desde la perspectiva del desarrollador, las fuentes de color suelen usarse de la misma manera que las fuentes monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="a9d58-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="a9d58-156">En los marcos XAML y Microsoft Edge, puede aplicar estilo al texto con fuentes de color de la misma manera que a las fuentes normales y, de forma predeterminada, el texto se representará en color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="a9d58-157">Sin embargo, si la aplicación llama directamente a las API de Direct2D (o a las API de Win2D) para representar texto, debe solicitar explícitamente la representación de fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="a9d58-158">Usar fuentes de color en una aplicación XAML</span><span class="sxs-lookup"><span data-stu-id="a9d58-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="a9d58-159">Los elementos de texto de la plataforma XAML (como [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)y [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) admiten fuentes de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9d58-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="a9d58-160">Simplemente puede aplicar estilo al texto con una fuente de color y cualquier glifo de color se representará en color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="a9d58-161">En el ejemplo de código siguiente se muestra una manera de aplicar estilo a un TextBlock con una fuente de color empaquetada con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9d58-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="a9d58-162">La misma técnica se aplica a las fuentes normales.</span><span class="sxs-lookup"><span data-stu-id="a9d58-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="a9d58-163">Si no desea que el elemento de texto XAML represente texto de colores multicolor, establezca la propiedad [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) en false.</span><span class="sxs-lookup"><span data-stu-id="a9d58-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="a9d58-164">Usar fuentes de color en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a9d58-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="a9d58-165">Las fuentes de color se representan de forma predeterminada en sitios web y aplicaciones web que se ejecutan en Microsoft Edge, incluido el control [WebView](/uwp/api/windows.ui.xaml.controls.webview) de XAML.</span><span class="sxs-lookup"><span data-stu-id="a9d58-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="a9d58-166">Simplemente use HTML y CSS para aplicar estilo al texto con una fuente de color y cualquier glifo de color se representará en color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="a9d58-167">Usar fuentes de color con DirectWrite y Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9d58-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="a9d58-168">La aplicación puede usar los métodos de dibujo de texto de nivel superior de Direct2D s ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) y [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)), o puede usar técnicas de nivel inferior para dibujar directamente las ejecuciones de glifos.</span><span class="sxs-lookup"><span data-stu-id="a9d58-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="a9d58-169">En cualquier caso, la aplicación requiere cambios en el código para poder controlar correctamente los glifos de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="a9d58-170">Si la aplicación usa las API de **DrawTextLayout** y **DrawText** de Direct2D s, tenga en cuenta que no representan glifos de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9d58-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="a9d58-171">Esto sirve para evitar cambios de comportamiento inesperados en las aplicaciones de representación de texto que se diseñaron antes de la compatibilidad con fuentes de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="a9d58-172">Para participar en la representación del glifo de color, pase la marca [**D2D1 \_ Draw \_ Text \_ Options \_ enable \_ color \_ Font**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) Options al método de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a9d58-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="a9d58-173">En el ejemplo de código siguiente se muestra cómo llamar al método DrawText de Direct2D s para representar una cadena en una fuente de color:</span><span class="sxs-lookup"><span data-stu-id="a9d58-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



<span data-ttu-id="a9d58-174">Si la aplicación usa las API de nivel inferior para controlar las ejecuciones de glifos directamente, seguirá funcionando en presencia de fuentes de color, pero no podrá dibujar glifos de color sin lógica adicional.</span><span class="sxs-lookup"><span data-stu-id="a9d58-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="a9d58-175">Para controlar correctamente los glifos de color, la aplicación debe:</span><span class="sxs-lookup"><span data-stu-id="a9d58-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="a9d58-176">Pase la información de ejecución del glifo a [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), junto con un parámetro de [**formatos de \_ \_ imagen \_ de glifo DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica qué tipos de glifo de color tiene la aplicación preparada para controlar.</span><span class="sxs-lookup"><span data-stu-id="a9d58-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="a9d58-177">Si hay glifos de color presentes (en función de la fuente y los **\_ formatos de \_ imagen \_ de glifo de DWRITE** solicitados), DirectWrite dividirá la ejecución del glifo principal en ejecuciones de glifos de color individuales a las que se puede tener acceso a través del objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) devuelto en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="a9d58-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="a9d58-178">Compruebe el HRESULT devuelto por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar si se ha detectado alguna ejecución del glifo de color.</span><span class="sxs-lookup"><span data-stu-id="a9d58-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="a9d58-179">Un **valor HRESULT** de **DWRITE \_ E \_ nocolor** indica que no hay ninguna ejecución del glifo de color aplicable.</span><span class="sxs-lookup"><span data-stu-id="a9d58-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="a9d58-180">Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informara de que no hay ejecuciones de glifos de color (devolviendo **DWRITE \_ E \_ nocolor**), toda la ejecución del glifo se trata como monocromática y la aplicación debe dibujarla como desee (por ejemplo, mediante [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="a9d58-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="a9d58-181">Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informa de la presencia de ejecuciones del glifo de color, la aplicación debe omitir la ejecución del glifo principal y, en su lugar, usar las ejecuciones del glifo de color devueltas por TranslateColorGlyphRun.</span><span class="sxs-lookup"><span data-stu-id="a9d58-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="a9d58-182">Para ello, recorra en iteración el objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) devuelto, recuperando cada glifo de color y dibuje según corresponda para su formato de imagen de glifo (por ejemplo, puede usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) y [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para dibujar glifos de mapa de bits de color y glifos SVG, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="a9d58-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="a9d58-183">En el ejemplo de código siguiente se muestra la estructura general de este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="a9d58-183">The following code example shows the general structure of this procedure:</span></span>


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="a9d58-184">Usar fuentes de color con Win2D</span><span class="sxs-lookup"><span data-stu-id="a9d58-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="a9d58-185">Al igual que en Direct2D, las API de dibujo de texto de Win2D s no representan glifos de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9d58-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="a9d58-186">Para participar en la representación del glifo de color, establezca la marca de opciones [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) en el objeto de formato de texto que la aplicación pasa al método de dibujo de texto.</span><span class="sxs-lookup"><span data-stu-id="a9d58-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="a9d58-187">En el ejemplo de código siguiente se muestra cómo representar una cadena en una fuente de color mediante Win2D:</span><span class="sxs-lookup"><span data-stu-id="a9d58-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a><span data-ttu-id="a9d58-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9d58-188">Related topics</span></span>

[<span data-ttu-id="a9d58-189">Ejemplo de glifo de color de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a9d58-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="a9d58-190">**Interfaz IDWriteFontFace4**</span><span class="sxs-lookup"><span data-stu-id="a9d58-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="a9d58-191">**IDWriteFactory4:: TranslateColorGlyphRun (método)**</span><span class="sxs-lookup"><span data-stu-id="a9d58-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="a9d58-192">**ID2D1DeviceContext4::D método rawText**</span><span class="sxs-lookup"><span data-stu-id="a9d58-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

