---
title: Sección Descripción
description: Sección Descripción
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Aspectos de Windows Media Player Mobile, sección Descripción
- aspectos, sección Descripción
- crear máscaras, sección Descripción
- escribir código para máscaras, sección Descripción
- Sección de descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903800"
---
# <a name="description-section"></a><span data-ttu-id="5c0ff-109">Sección Descripción</span><span class="sxs-lookup"><span data-stu-id="5c0ff-109">Description Section</span></span>

<span data-ttu-id="5c0ff-110">A continuación, debe proporcionar una sección que describa el tamaño y la orientación de la máscara al crear una máscara para Windows Media Player 9 series para Windows Mobile 2003 y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="5c0ff-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="5c0ff-111">La sección Descripción debe empezar con la palabra Description entre corchetes y, a continuación, incluir una línea que especifique las dimensiones y la resolución de pantalla de la máscara.</span><span class="sxs-lookup"><span data-stu-id="5c0ff-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="5c0ff-112">Las líneas que comienzan con dos barras diagonales no se procesan y se pueden usar para comentarios o, como se muestra en el código anterior, una plantilla para ayudarle a recordar lo que ocurre en una sección.</span><span class="sxs-lookup"><span data-stu-id="5c0ff-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="5c0ff-113">También puede usar plantillas para ayudar a alinear todo en las columnas.</span><span class="sxs-lookup"><span data-stu-id="5c0ff-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="5c0ff-114">Para obtener más información sobre la sección de descripción, vea [Descripción](description.md) en la referencia de la máscara.</span><span class="sxs-lookup"><span data-stu-id="5c0ff-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c0ff-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c0ff-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c0ff-116">**Escritura del código**</span><span class="sxs-lookup"><span data-stu-id="5c0ff-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




