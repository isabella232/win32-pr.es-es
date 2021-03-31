---
title: Usar bordes en paquetes de descarga de Windows Media (en desuso)
description: Usar bordes en paquetes de descarga de Windows Media (en desuso)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- bordes, acerca de
- Paquetes de descarga de Windows Media, bordes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418791"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="72bee-109">Usar bordes en paquetes de descarga de Windows Media (en desuso)</span><span class="sxs-lookup"><span data-stu-id="72bee-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="72bee-110">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="72bee-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="72bee-111">Los bordes permiten crear una interfaz gráfica de usuario personalizada para el contenido empaquetado.</span><span class="sxs-lookup"><span data-stu-id="72bee-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="72bee-112">El borde puede incluir elementos como imágenes, controles interactivos y vínculos a sitios Web.</span><span class="sxs-lookup"><span data-stu-id="72bee-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="72bee-113">Puede usar bordes en los casos en los que desee agregar un valor adicional al contenido empaquetado, como para la personalización de marca o el anuncio.</span><span class="sxs-lookup"><span data-stu-id="72bee-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="72bee-114">Después de que los usuarios descarguen y abran el paquete de descarga de Windows Media, Windows Media Player muestra automáticamente el borde personalizado cuando reproduce el contenido empaquetado.</span><span class="sxs-lookup"><span data-stu-id="72bee-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="72bee-115">A diferencia de una máscara, que permite a los usuarios reemplazar por completo la interfaz de usuario de Windows Media Player, solo se muestra un borde en el panel **reproducción en curso** del reproductor en modo completo.</span><span class="sxs-lookup"><span data-stu-id="72bee-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="72bee-116">Sin embargo, las mismas herramientas y tecnologías que se usan para crear máscaras también se usan para crear bordes.</span><span class="sxs-lookup"><span data-stu-id="72bee-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="72bee-117">En la ilustración siguiente se muestra un borde.</span><span class="sxs-lookup"><span data-stu-id="72bee-117">The following illustration shows a border.</span></span>

![un borde mostrado en el reproductor de Windows Media 10](images/border-v10.png)

<span data-ttu-id="72bee-119">Es importante comprender las técnicas básicas para crear una máscara antes de intentar crear un borde.</span><span class="sxs-lookup"><span data-stu-id="72bee-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="72bee-120">La programación de bordes se consigue con dos lenguajes de programación: lenguaje de marcado extensible (XML) y Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="72bee-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="72bee-121">XML se utiliza para definir elementos de interfaz como botones, controles deslizantes y cuadros de texto.</span><span class="sxs-lookup"><span data-stu-id="72bee-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="72bee-122">No es necesario comprender todos los detalles de XML, ya que no es necesario escribir nuevos elementos de código XML. puede simplemente usar los proporcionados por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="72bee-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="72bee-123">Aunque JScript no es necesario para crear bordes, se puede usar para proporcionar funcionalidad adicional.</span><span class="sxs-lookup"><span data-stu-id="72bee-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="72bee-124">Un archivo de borde comprimido con la extensión de nombre de archivo. WMZ incluye un archivo de definición de borde con una extensión de nombre de archivo. WMS y todos los archivos de imagen que se usan dentro del borde.</span><span class="sxs-lookup"><span data-stu-id="72bee-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="72bee-125">Para incluir un borde en un paquete de descarga de Windows Media, basta con crear un borde y hacer referencia a ese borde en una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="72bee-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="72bee-126">El archivo de borde se carga en Windows Media Player después de que el reproductor analice el metarchivo e interprete el elemento de **máscara** que hace referencia al borde.</span><span class="sxs-lookup"><span data-stu-id="72bee-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="72bee-127">El elemento **Skin** solo se usa para los bordes y el atributo href del elemento **Skin** solo puede hacer referencia a una máscara para cada paquete.</span><span class="sxs-lookup"><span data-stu-id="72bee-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72bee-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72bee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72bee-129">**Bordes de Media Player de Windows (desusado)**</span><span class="sxs-lookup"><span data-stu-id="72bee-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="72bee-130">**Paquetes de descarga de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="72bee-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="72bee-131">**Máscaras de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="72bee-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




