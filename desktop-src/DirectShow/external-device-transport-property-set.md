---
description: Conjunto de propiedades de transporte de dispositivos externos
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propiedades de transporte de dispositivos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909223"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="33f70-103">Conjunto de propiedades de transporte de dispositivos externos</span><span class="sxs-lookup"><span data-stu-id="33f70-103">External Device Transport Property Set</span></span>

<span data-ttu-id="33f70-104">Este conjunto de propiedades controla el transporte de datos hacia y desde un dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="33f70-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="33f70-105">En la mayoría de los casos, las aplicaciones no deben usar directamente este conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="33f70-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="33f70-106">Use la [**interfaz IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="33f70-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="33f70-107">En la tabla siguiente se enumeran las propiedades que son relevantes para las aplicaciones en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="33f70-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="33f70-108">Para obtener una descripción completa de este conjunto de propiedades, consulte el DDK del Kit de desarrollo de controladores de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="33f70-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="33f70-109">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="33f70-109">Label</span></span> | <span data-ttu-id="33f70-110">Value</span><span class="sxs-lookup"><span data-stu-id="33f70-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="33f70-111">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="33f70-111">Property Set GUID</span></span> | <span data-ttu-id="33f70-112">TRANSPORTE EXT DE PROPSETID \_ \_</span><span class="sxs-lookup"><span data-stu-id="33f70-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="33f70-113">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="33f70-113">Property ID</span></span>                                                                           | <span data-ttu-id="33f70-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="33f70-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="33f70-115">**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**</span><span class="sxs-lookup"><span data-stu-id="33f70-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="33f70-116">Busca un número de seguimiento absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="33f70-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="33f70-117">**BÚSQUEDA DE CÓDIGO \_ DE TIEMPO DE EXTXPORT \_ DE KSPROPERTY \_**</span><span class="sxs-lookup"><span data-stu-id="33f70-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="33f70-118">Busca un código de hora.</span><span class="sxs-lookup"><span data-stu-id="33f70-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="33f70-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33f70-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f70-120">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="33f70-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



