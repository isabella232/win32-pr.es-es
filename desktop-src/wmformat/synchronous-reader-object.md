---
title: Objeto del lector sincrónico
description: Objeto del lector sincrónico
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- SDK de Windows Media Format, objetos de lector sincrónicos
- Advanced Systems Format (ASF), objetos de lector sincrónicos
- ASF (formato de sistemas avanzados), objetos de lector sincrónicos
- objetos, objetos de lectura sincrónicos
- lectores sincrónicos, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704918"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="c73df-108">Objeto del lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="c73df-108">Synchronous Reader Object</span></span>

<span data-ttu-id="c73df-109">El objeto lector sincrónico se utiliza para leer archivos multimedia digitales mediante llamadas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="c73df-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="c73df-110">La función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)crea el objeto de lector sincrónico, que establece un puntero a una interfaz **IWMSyncReader** .</span><span class="sxs-lookup"><span data-stu-id="c73df-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="c73df-111">Las otras interfaces que admite la interfaz de lectura sincrónica se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c73df-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="c73df-112">El objeto lector sincrónico admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="c73df-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="c73df-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c73df-113">Interface</span></span>                                | <span data-ttu-id="c73df-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c73df-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c73df-115">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="c73df-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="c73df-116">Establece y recupera información de encabezado, como metadatos, [*marcadores*](wmformat-glossary.md), etc.</span><span class="sxs-lookup"><span data-stu-id="c73df-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="c73df-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="c73df-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="c73df-118">Enumera la información de códec disponible.</span><span class="sxs-lookup"><span data-stu-id="c73df-118">Enumerates the available codec information.</span></span> <span data-ttu-id="c73df-119">Hereda todos los métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="c73df-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="c73df-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="c73df-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="c73df-121">Admite tamaños de atributo grandes, nombres de atributos duplicados y compatibilidad con varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="c73df-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="c73df-122">Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="c73df-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="c73df-123">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="c73df-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="c73df-124">Proporciona acceso a la información de perfil del archivo de Windows Media cargado en el lector.</span><span class="sxs-lookup"><span data-stu-id="c73df-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="c73df-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="c73df-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="c73df-126">Recupera el identificador único global (GUID), si existe, asociado al perfil.</span><span class="sxs-lookup"><span data-stu-id="c73df-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="c73df-127">Hereda todos los métodos de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="c73df-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="c73df-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="c73df-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="c73df-129">Admite el uso compartido de ancho de banda y la información de priorización de flujo en el perfil.</span><span class="sxs-lookup"><span data-stu-id="c73df-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="c73df-130">Hereda todos los métodos de **IWMProfile** y **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="c73df-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="c73df-131">**IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="c73df-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="c73df-132">Proporciona capacidades de lectura sincrónica para archivos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="c73df-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="c73df-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="c73df-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="c73df-134">Proporciona compatibilidad para buscar códigos de tiempo SMPTE y para asignar ejemplos manualmente.</span><span class="sxs-lookup"><span data-stu-id="c73df-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="c73df-135">Hereda todos los métodos de **IWMSyncReader**.</span><span class="sxs-lookup"><span data-stu-id="c73df-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="c73df-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c73df-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73df-137">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="c73df-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="c73df-138">**Objeto del lector**</span><span class="sxs-lookup"><span data-stu-id="c73df-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="c73df-139">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="c73df-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




