---
description: El objeto SummaryInfo se usa para leer, crear y actualizar propiedades de documento desde la secuencia de información de Resumen de un objeto de almacenamiento.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: SummaryInfo (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653731"
---
# <a name="summaryinfo-object"></a><span data-ttu-id="c8736-103">SummaryInfo (objeto)</span><span class="sxs-lookup"><span data-stu-id="c8736-103">SummaryInfo object</span></span>

<span data-ttu-id="c8736-104">El objeto **SummaryInfo** se usa para leer, crear y actualizar propiedades de documento desde la [secuencia de información de Resumen](summary-information-stream.md) de un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c8736-104">The **SummaryInfo** object is used to read, create, and update document properties from the [summary information stream](summary-information-stream.md) of a storage object.</span></span>

## <a name="members"></a><span data-ttu-id="c8736-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8736-105">Members</span></span>

<span data-ttu-id="c8736-106">El objeto **SummaryInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8736-106">The **SummaryInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="c8736-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8736-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8736-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8736-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8736-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8736-109">Methods</span></span>

<span data-ttu-id="c8736-110">El objeto **SummaryInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c8736-110">The **SummaryInfo** object has these methods.</span></span>



| <span data-ttu-id="c8736-111">Método</span><span class="sxs-lookup"><span data-stu-id="c8736-111">Method</span></span>                                 | <span data-ttu-id="c8736-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8736-112">Description</span></span>                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8736-113">**Persist**</span><span class="sxs-lookup"><span data-stu-id="c8736-113">**Persist**</span></span>](summaryinfo-persist.md) | <span data-ttu-id="c8736-114">Da formato y escribe las propiedades previamente almacenadas en la [secuencia de información de Resumen](summary-information-stream.md)estándar.</span><span class="sxs-lookup"><span data-stu-id="c8736-114">Formats and writes the previously stored properties into the standard [summary information stream](summary-information-stream.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c8736-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8736-115">Properties</span></span>

<span data-ttu-id="c8736-116">El objeto **SummaryInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c8736-116">The **SummaryInfo** object has these properties.</span></span>



| <span data-ttu-id="c8736-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8736-117">Property</span></span>                                                                             | <span data-ttu-id="c8736-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8736-118">Description</span></span>                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8736-119">**Propiedad Property (objeto SummaryInfo)**</span><span class="sxs-lookup"><span data-stu-id="c8736-119">**Property Property (SummaryInfo Object)**</span></span>](summaryinfo-summaryinfo.md)<br/> | <span data-ttu-id="c8736-120">Obtiene o establece el valor de la propiedad especificada en la secuencia de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="c8736-120">Gets or sets the value for the specified property in the summary information stream.</span></span><br/> |
| [<span data-ttu-id="c8736-121">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="c8736-121">**PropertyCount**</span></span>](summaryinfo-propertycount.md)<br/>                        | <span data-ttu-id="c8736-122">Indica el número actual de valores de propiedad en el objeto de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="c8736-122">Indicates the current number of property values in the summary information object.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c8736-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8736-123">Requirements</span></span>



| <span data-ttu-id="c8736-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8736-124">Requirement</span></span> | <span data-ttu-id="c8736-125">Value</span><span class="sxs-lookup"><span data-stu-id="c8736-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8736-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c8736-126">Version</span></span><br/> | <span data-ttu-id="c8736-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8736-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c8736-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8736-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c8736-129">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8736-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c8736-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8736-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8736-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8736-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c8736-132">IID</span><span class="sxs-lookup"><span data-stu-id="c8736-132">IID</span></span><br/>     | <span data-ttu-id="c8736-133">IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c8736-133">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="c8736-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8736-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8736-135">**Propiedad SummaryInformation (objeto Database)**</span><span class="sxs-lookup"><span data-stu-id="c8736-135">**SummaryInformation Property (Database Object)**</span></span>](database-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="c8736-136">**Propiedad SummaryInformation (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="c8736-136">**SummaryInformation Property (Installer Object)**</span></span>](installer-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="c8736-137">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c8736-137">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




