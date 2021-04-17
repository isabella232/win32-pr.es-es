---
description: Todos los objetos de elemento tienen propiedades.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Atributos de propiedad (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497548"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="861fe-103">Atributos de propiedad (WIA)</span><span class="sxs-lookup"><span data-stu-id="861fe-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="861fe-104">Todos los objetos de elemento tienen propiedades.</span><span class="sxs-lookup"><span data-stu-id="861fe-104">All item objects have properties.</span></span> <span data-ttu-id="861fe-105">Las propiedades tienen atributos.</span><span class="sxs-lookup"><span data-stu-id="861fe-105">The properties have attributes.</span></span> <span data-ttu-id="861fe-106">Por ejemplo, los atributos de propiedad indican si una propiedad se lee, se escribe o se elimina.</span><span class="sxs-lookup"><span data-stu-id="861fe-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="861fe-107">También indican los valores de propiedad válidos.</span><span class="sxs-lookup"><span data-stu-id="861fe-107">They also indicate the valid property values.</span></span> <span data-ttu-id="861fe-108">Las constantes siguientes son atributos de propiedad válidos:</span><span class="sxs-lookup"><span data-stu-id="861fe-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="861fe-109">Atributo de propiedad</span><span class="sxs-lookup"><span data-stu-id="861fe-109">Property Attribute</span></span>        | <span data-ttu-id="861fe-110">Significado</span><span class="sxs-lookup"><span data-stu-id="861fe-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="861fe-111">propiedades de WIA que se \_ \_ almacenan en caché</span><span class="sxs-lookup"><span data-stu-id="861fe-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="861fe-112">El dispositivo puede almacenar en caché el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="861fe-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="861fe-113">\_marca de prop de WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="861fe-114">La propiedad tiene una lista de valores de marca válidos.</span><span class="sxs-lookup"><span data-stu-id="861fe-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="861fe-115">Los valores de marca se combinan mediante una operación **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="861fe-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="861fe-116">\_lista de propiedades de WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="861fe-117">La propiedad tiene una lista de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="861fe-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="861fe-118">no se ha \_ propl de WIA \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="861fe-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="861fe-119">La propiedad no tiene ningún valor válido asociado a ella.</span><span class="sxs-lookup"><span data-stu-id="861fe-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="861fe-120">\_intervalo de propiedades de WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="861fe-121">La propiedad tiene un intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="861fe-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="861fe-122">lectura de la \_ prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="861fe-123">La aplicación puede leer el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="861fe-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="861fe-124">propiedades de WIA de WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="861fe-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="861fe-125">La aplicación puede leer y escribir el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="861fe-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="861fe-126">se \_ \_ requiere la sincronización de propiedades de WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="861fe-127">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="861fe-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="861fe-128">\_escritura de propiedades de WIA \_</span><span class="sxs-lookup"><span data-stu-id="861fe-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="861fe-129">La aplicación puede escribir el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="861fe-129">The application can write the property's value.</span></span>                                                          |



 

 

 



