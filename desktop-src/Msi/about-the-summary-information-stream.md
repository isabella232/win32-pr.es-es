---
description: La secuencia de información de Resumen contiene información sobre el paquete que se puede ver a través del explorador de Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Acerca del flujo de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156356"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="0490d-103">Acerca del flujo de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="0490d-103">About the Summary Information Stream</span></span>

<span data-ttu-id="0490d-104">La secuencia de información de Resumen contiene información sobre el paquete que se puede ver a través del explorador de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0490d-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="0490d-105">Esta información es accesible a través de la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0490d-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="0490d-106">Es el autor quien debe proporcionar los valores de cada una de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0490d-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="0490d-107">La secuencia de información de Resumen utiliza COM para proporcionar almacenamiento estructurado de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="0490d-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="0490d-108">COM admite el concepto de almacenamiento estructurado accesible a través de la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0490d-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="0490d-109">El almacenamiento estructurado, a su vez, admite el concepto de conjuntos de propiedades como un método flexible para serializar casi cualquier información.</span><span class="sxs-lookup"><span data-stu-id="0490d-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="0490d-110">La especificación COM define un conjunto de propiedades estándar único, información de Resumen, que se usa para rellenar las hojas de propiedades visibles desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0490d-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="0490d-111">Por lo tanto, los usuarios pueden ver la información almacenada en la secuencia de información de resumen al hacer clic con el botón secundario en una base de datos del instalador o en transformar y seleccionar [propiedades](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0490d-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="0490d-112">Para obtener una lista del conjunto de propiedades de Resumen, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="0490d-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="0490d-113">Para obtener breves descripciones de las propiedades de información de Resumen utilizadas con las bases de datos, las transformaciones y las revisiones, vea [descripciones de propiedades de Resumen](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="0490d-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



