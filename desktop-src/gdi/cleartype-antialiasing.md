---
description: El suavizado de contorno de ClearType de Microsoft es un método de suavizado que mejora la resolución de la presentación de fuentes sobre el suavizado de contorno tradicional.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Suavizado de contorno de ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985047"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="baa5f-103">Suavizado de contorno de ClearType</span><span class="sxs-lookup"><span data-stu-id="baa5f-103">ClearType Antialiasing</span></span>

<span data-ttu-id="baa5f-104">El suavizado de contorno de ClearType de Microsoft es un método de suavizado que mejora la resolución de la presentación de fuentes sobre el suavizado de contorno tradicional.</span><span class="sxs-lookup"><span data-stu-id="baa5f-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="baa5f-105">Mejora drásticamente la legibilidad en monitores LCD de color con una interfaz digital, como los equipos portátiles y las pantallas de escritorio plano de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="baa5f-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="baa5f-106">La legibilidad en pantallas de CRT también se ha mejorado en cierto modo.</span><span class="sxs-lookup"><span data-stu-id="baa5f-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="baa5f-107">Sin embargo, ClearType depende de la orientación y el orden de las franjas LCD.</span><span class="sxs-lookup"><span data-stu-id="baa5f-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="baa5f-108">Actualmente, ClearType solo se implementa para los monitores de LCD con bandas verticales que se ordenan por RGB.</span><span class="sxs-lookup"><span data-stu-id="baa5f-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="baa5f-109">En concreto, esto afecta a los Tablet PC, donde la pantalla se puede orientar en cualquier dirección y a las pantallas que se pueden convertir de horizontal a vertical.</span><span class="sxs-lookup"><span data-stu-id="baa5f-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="baa5f-110">Se permite el suavizado de contorno de ClearType:</span><span class="sxs-lookup"><span data-stu-id="baa5f-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="baa5f-111">Para el color de 16, 24 y 32 bits (deshabilitado para 256 colores o menos)</span><span class="sxs-lookup"><span data-stu-id="baa5f-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="baa5f-112">Para DC de pantalla y DC de memoria (no para el DC de impresora)</span><span class="sxs-lookup"><span data-stu-id="baa5f-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="baa5f-113">Para fuentes TrueType y fuentes OpenType con esquemas TrueType</span><span class="sxs-lookup"><span data-stu-id="baa5f-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="baa5f-114">El suavizado de contorno de ClearType está deshabilitado:</span><span class="sxs-lookup"><span data-stu-id="baa5f-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="baa5f-115">En cliente de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="baa5f-115">Under terminal server client</span></span>
-   <span data-ttu-id="baa5f-116">Para fuentes de mapa de bits, fuentes vectoriales, fuentes de dispositivo, fuentes de tipo 1 o fuentes OpenType PostScript sin contornos TrueType</span><span class="sxs-lookup"><span data-stu-id="baa5f-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="baa5f-117">Si la fuente ha optimizado los mapas de bits incrustados, solo para aquellos tamaños de fuente que contengan los mapas de bits incrustados</span><span class="sxs-lookup"><span data-stu-id="baa5f-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="baa5f-118">Para activar el suavizado de contorno de ClearType, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una vez para activar el suavizado de fuentes y, después, una segunda vez para establecer el tipo de suavizado en fe \_ FONTSMOOTHINGCLEARTYPE, como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="baa5f-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="baa5f-119">Puede ajustar el aspecto del texto cambiando el valor de contraste utilizado en el algoritmo ClearType.</span><span class="sxs-lookup"><span data-stu-id="baa5f-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="baa5f-120">El valor predeterminado es 1.400, pero puede ser cualquier valor entre 1.000 y 2.200.</span><span class="sxs-lookup"><span data-stu-id="baa5f-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="baa5f-121">En función del dispositivo de pantalla y la sensibilidad del usuario a los colores, un valor de contraste mayor o menor puede mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="baa5f-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="baa5f-122">Para cambiar el contraste, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST.</span><span class="sxs-lookup"><span data-stu-id="baa5f-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="baa5f-123">En el código siguiente se establece el valor de contraste en 1.600.</span><span class="sxs-lookup"><span data-stu-id="baa5f-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="baa5f-124">Debe tener en cuenta los siguientes detalles para la compatibilidad de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="baa5f-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="baa5f-125">La representación de texto con ClearType es ligeramente más lenta que con el suavizado de contorno estándar.</span><span class="sxs-lookup"><span data-stu-id="baa5f-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="baa5f-126">Las aplicaciones no deben usar XOR para mostrar el texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="baa5f-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="baa5f-127">Las aplicaciones deben establecer el color de fondo y volver a mostrar el texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="baa5f-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="baa5f-128">Las aplicaciones no deben pintar el mismo texto sobre sí mismo en modo transparente.</span><span class="sxs-lookup"><span data-stu-id="baa5f-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="baa5f-129">Si esto ocurre, los píxeles del borde con suavizado de contorno establecerán la combinación de colores en lugar de con el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="baa5f-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="baa5f-130">Esto da como resultado bordes oscurecidos y multicolor.</span><span class="sxs-lookup"><span data-stu-id="baa5f-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="baa5f-131">Las aplicaciones no deben pintar texto pintando los caracteres individualmente en el modo opaco porque el borde de un carácter puede recortarse por el siguiente carácter.</span><span class="sxs-lookup"><span data-stu-id="baa5f-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="baa5f-132">Esto se debe a que un carácter suavizado con ClearType puede tener un ancho negativo A o C, donde el carácter normal tiene un ancho positivo o de C.</span><span class="sxs-lookup"><span data-stu-id="baa5f-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="baa5f-133">Solo se garantiza que el ancho B del carácter es el mismo.</span><span class="sxs-lookup"><span data-stu-id="baa5f-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="baa5f-134">Del mismo modo, las aplicaciones deben tener cuidado si el texto suavizado está junto al texto sin suavizar.</span><span class="sxs-lookup"><span data-stu-id="baa5f-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="baa5f-135">Si una aplicación representa texto y, a continuación, manipula el mapa de bits, el suavizado de fuentes debe desactivarse estableciendo el miembro **lfQuality** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) en NONANTIALIASED \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="baa5f-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="baa5f-136">Por ejemplo, un juego puede Agregar un efecto de sombra de mapa de bits o el texto representado en un mapa de bits se puede escalar para generar un ThumbView.</span><span class="sxs-lookup"><span data-stu-id="baa5f-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="baa5f-137">Si el usuario se ejecuta en modo vertical (es decir, la segmentación del monitor es horizontal), se debe deshabilitar el suavizado de contorno de ClearType.</span><span class="sxs-lookup"><span data-stu-id="baa5f-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="baa5f-138">El parámetro *fdwQuality* de [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) y el miembro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceptan la marca de calidad de CLEARTYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="baa5f-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="baa5f-139">La rasterización de las fuentes creadas con esta marca usará el rasterizador de ClearType.</span><span class="sxs-lookup"><span data-stu-id="baa5f-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="baa5f-140">Esta marca no tiene ningún efecto en las versiones anteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="baa5f-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
