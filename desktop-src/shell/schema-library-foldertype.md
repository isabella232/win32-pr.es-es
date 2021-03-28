---
description: El <folderType> elemento especifica un GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe; de lo contrario, es opcional. Este elemento no tiene atributos ni elementos secundarios.
title: Elemento folderType (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984590"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="3b276-105">Elemento folderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="3b276-106">El <folderType> elemento especifica un GUID para el tipo de carpeta.</span><span class="sxs-lookup"><span data-stu-id="3b276-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="3b276-107">Este elemento es necesario si el <templateInfo> elemento existe; de lo contrario, es opcional.</span><span class="sxs-lookup"><span data-stu-id="3b276-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="3b276-108">Este elemento no tiene atributos ni elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="3b276-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b276-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b276-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="3b276-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3b276-110">Element Information</span></span>



| <span data-ttu-id="3b276-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3b276-111">Parent Element</span></span>                                                           | <span data-ttu-id="3b276-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b276-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="3b276-113">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="3b276-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b276-114">Remarks</span></span>

<span data-ttu-id="3b276-115">La configuración de un tipo de carpeta determina las columnas y los detalles que aparecen en el explorador de Windows de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b276-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="3b276-116">Los identificadores de tipo de carpeta ([**FOLDERTYPEID**](foldertypeid.md)) son GUID definidos en Shlguid. h.</span><span class="sxs-lookup"><span data-stu-id="3b276-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="3b276-117">En la tabla siguiente se enumeran los GUID de tipos de carpetas comunes.</span><span class="sxs-lookup"><span data-stu-id="3b276-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="3b276-118">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="3b276-118">Folder Type</span></span>      | <span data-ttu-id="3b276-119">GUID</span><span class="sxs-lookup"><span data-stu-id="3b276-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="3b276-120">Biblioteca genérica</span><span class="sxs-lookup"><span data-stu-id="3b276-120">Generic Library</span></span>  | <span data-ttu-id="3b276-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="3b276-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="3b276-122">Bibliotecas de usuarios</span><span class="sxs-lookup"><span data-stu-id="3b276-122">Users Libraries</span></span>  | <span data-ttu-id="3b276-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="3b276-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="3b276-124">Carpeta documentos</span><span class="sxs-lookup"><span data-stu-id="3b276-124">Documents Folder</span></span> | <span data-ttu-id="3b276-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="3b276-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="3b276-126">Carpeta imágenes</span><span class="sxs-lookup"><span data-stu-id="3b276-126">Pictures Folder</span></span>  | <span data-ttu-id="3b276-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="3b276-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="3b276-128">Carpeta de vídeos</span><span class="sxs-lookup"><span data-stu-id="3b276-128">Videos Folder</span></span>    | <span data-ttu-id="3b276-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="3b276-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="3b276-130">Carpeta Juegos</span><span class="sxs-lookup"><span data-stu-id="3b276-130">Games Folder</span></span>     | <span data-ttu-id="3b276-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="3b276-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="3b276-132">Carpeta música</span><span class="sxs-lookup"><span data-stu-id="3b276-132">Music Folder</span></span>     | <span data-ttu-id="3b276-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="3b276-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="3b276-134">Contactos</span><span class="sxs-lookup"><span data-stu-id="3b276-134">Contacts</span></span>         | <span data-ttu-id="3b276-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="3b276-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3b276-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b276-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b276-137">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="3b276-138">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="3b276-139">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="3b276-140">Name (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="3b276-141">Elemento ownerSID (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="3b276-142">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="3b276-143">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="3b276-144">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="3b276-145">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="3b276-146">version (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="3b276-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



