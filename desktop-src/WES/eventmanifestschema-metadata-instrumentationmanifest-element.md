---
title: Elemento metadata (instrumentationManifest)
description: Contiene valores globales a los que se puede hacer referencia en otros manifiestos.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- elemento de metadatos EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149919"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="dedc1-104">Elemento metadata (instrumentationManifest)</span><span class="sxs-lookup"><span data-stu-id="dedc1-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="dedc1-105">Contiene valores globales a los que se puede hacer referencia en otros manifiestos.</span><span class="sxs-lookup"><span data-stu-id="dedc1-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="dedc1-106">Para obtener un ejemplo, vea el archivo Winmeta.xml incluido en la \\ carpeta include del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dedc1-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="dedc1-107">El elemento de **metadatos** se define mediante el elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dedc1-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="dedc1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dedc1-108">Remarks</span></span>

<span data-ttu-id="dedc1-109">Aunque puede crear un manifiesto que contiene una sección de metadatos, el servicio no lo usará; los únicos metadatos que reconoce el servicio son los metadatos que se encuentran en el archivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="dedc1-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedc1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedc1-110">Requirements</span></span>



| <span data-ttu-id="dedc1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedc1-111">Requirement</span></span> | <span data-ttu-id="dedc1-112">Value</span><span class="sxs-lookup"><span data-stu-id="dedc1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dedc1-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dedc1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dedc1-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dedc1-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dedc1-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dedc1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dedc1-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dedc1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dedc1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="dedc1-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="dedc1-118">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="dedc1-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="dedc1-119">**instrumentationManifest**</span><span class="sxs-lookup"><span data-stu-id="dedc1-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





