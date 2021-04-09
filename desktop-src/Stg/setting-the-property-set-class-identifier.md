---
title: Establecimiento del identificador de clase del conjunto de propiedades
description: El método IPropertyStorage SetClass establece el CLSID del objeto de almacenamiento y el valor de la etiqueta de clase almacenados en el conjunto de propiedades COM. Esto sucede cuando se invoca en un almacenamiento de propiedades no simple almacenado en un objeto de almacenamiento estructurado.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Establecimiento del identificador de clase del conjunto de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076163"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="e37a9-105">Establecimiento del identificador de clase del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e37a9-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="e37a9-106">El método [**IPropertyStorage:: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) establece el CLSID del objeto de almacenamiento y el valor de la etiqueta de clase almacenados en el conjunto de propiedades com.</span><span class="sxs-lookup"><span data-stu-id="e37a9-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="e37a9-107">Esto sucede cuando se invoca en un almacenamiento de propiedades no simple almacenado en un objeto de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="e37a9-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="e37a9-108">Esto proporciona coherencia y uniformidad, lo que crea una interacción mejor con algunas herramientas.</span><span class="sxs-lookup"><span data-stu-id="e37a9-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="e37a9-109">Un objeto de almacenamiento de propiedades no es simple si se crea llamando a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con el marcador de **PROPSETFLAG no \_ simple** establecido.</span><span class="sxs-lookup"><span data-stu-id="e37a9-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="e37a9-110">El CLSID del objeto de almacenamiento se establece con una llamada a [**IStorage:: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span><span class="sxs-lookup"><span data-stu-id="e37a9-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




