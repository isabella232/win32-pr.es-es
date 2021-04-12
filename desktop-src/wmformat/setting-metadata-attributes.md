---
title: Establecer atributos de metadatos
description: Establecer atributos de metadatos
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- SDK de Windows Media Format, establecer atributos de metadatos
- Advanced Systems Format (ASF), establecer atributos de metadatos
- ASF (formato de sistemas avanzados), establecer atributos de metadatos
- metadatos, establecer atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420305"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="0f405-107">Establecer atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="0f405-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="0f405-108">Los atributos de metadatos se establecen mediante el método [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .</span><span class="sxs-lookup"><span data-stu-id="0f405-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="0f405-109">Todos los atributos se asignan a un idioma de la lista de idiomas del archivo.</span><span class="sxs-lookup"><span data-stu-id="0f405-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="0f405-110">Puede tener acceso a la lista de idiomas mediante la interfaz [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) .</span><span class="sxs-lookup"><span data-stu-id="0f405-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="0f405-111">Para obtener un puntero a una interfaz **IWMLanguageList** , llame a **QueryInterface** en cualquier interfaz del objeto desde el que haya obtenido [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span><span class="sxs-lookup"><span data-stu-id="0f405-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="0f405-112">Puede agregar atributos con cualquier nombre que desee.</span><span class="sxs-lookup"><span data-stu-id="0f405-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="0f405-113">Sin embargo, el uso de nombres de atributo que no son nombres estándar compatibles con el SDK de Windows Media Format puede dificultar la detección de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="0f405-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="0f405-114">La mayoría de las aplicaciones de reproducción multimedia comprobarán los valores estándar.</span><span class="sxs-lookup"><span data-stu-id="0f405-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="0f405-115">Para obtener más información, vea [metadatos personalizados](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="0f405-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="0f405-116">No se puede usar el número de secuencia 0xFFFF para agregar un atributo globalmente.</span><span class="sxs-lookup"><span data-stu-id="0f405-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="0f405-117">Debe asignar cada atributo a un número de secuencia específico o a la secuencia 0 para los atributos de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="0f405-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f405-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f405-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f405-119">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="0f405-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




