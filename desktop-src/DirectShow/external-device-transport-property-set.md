---
description: Conjunto de propiedades de transporte de dispositivo externo
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propiedades de transporte de dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152696"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="aa944-103">Conjunto de propiedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="aa944-103">External Device Transport Property Set</span></span>

<span data-ttu-id="aa944-104">Este conjunto de propiedades controla el transporte de datos hacia y desde un dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="aa944-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="aa944-105">En la mayoría de los casos, las aplicaciones no deben utilizar directamente esta propiedad establecida.</span><span class="sxs-lookup"><span data-stu-id="aa944-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="aa944-106">En su lugar, use la interfaz [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="aa944-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="aa944-107">En la tabla siguiente se enumeran las propiedades que son relevantes para las aplicaciones de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="aa944-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="aa944-108">Para obtener una descripción completa de este conjunto de propiedades, consulte el DDK del kit de desarrollo de controladores de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa944-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="aa944-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="aa944-109">Property Set GUID</span></span> | <span data-ttu-id="aa944-110">\_transporte ext \_ PROPSETID</span><span class="sxs-lookup"><span data-stu-id="aa944-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="aa944-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="aa944-111">Property ID</span></span>                                                                           | <span data-ttu-id="aa944-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa944-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="aa944-113">**búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_**</span><span class="sxs-lookup"><span data-stu-id="aa944-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="aa944-114">Busca un número de pista absoluta (ATN).</span><span class="sxs-lookup"><span data-stu-id="aa944-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="aa944-115">**KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_**</span><span class="sxs-lookup"><span data-stu-id="aa944-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="aa944-116">Busca un código de hora.</span><span class="sxs-lookup"><span data-stu-id="aa944-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="aa944-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa944-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa944-118">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="aa944-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



