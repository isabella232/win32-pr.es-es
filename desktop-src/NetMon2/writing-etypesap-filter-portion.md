---
description: La parte de ETYPE/SAP del filtro de captura notifica al controlador de Monitor de red para que acepte fotogramas que tengan una combinación específica de ETYPE y puntos de acceso de servicio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Escribir la parte de filtro de ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002555"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="9f8b5-103">Escribir la parte de filtro de ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="9f8b5-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="9f8b5-104">La parte de ETYPE/SAP del filtro de captura notifica al controlador de Monitor de red para que acepte fotogramas que tengan una combinación específica de ETYPE y [*puntos de acceso de servicio*](s.md) (SAP).</span><span class="sxs-lookup"><span data-stu-id="9f8b5-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="9f8b5-105">ETYPE y SAP son formas en que los protocolos de bajo nivel, como Ethernet, LLC y Snap, indican qué protocolo los sigue.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="9f8b5-106">De manera específica:</span><span class="sxs-lookup"><span data-stu-id="9f8b5-106">Specifically:</span></span>

-   <span data-ttu-id="9f8b5-107">Ethernet especifica un ETYPE</span><span class="sxs-lookup"><span data-stu-id="9f8b5-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="9f8b5-108">LLC especifica un SAP</span><span class="sxs-lookup"><span data-stu-id="9f8b5-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="9f8b5-109">Ajustar especifica un ETYPE</span><span class="sxs-lookup"><span data-stu-id="9f8b5-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="9f8b5-110">ETYPE/marcas de filtro de captura de SAP</span><span class="sxs-lookup"><span data-stu-id="9f8b5-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="9f8b5-111">Utilice la siguiente información para establecer las marcas en el miembro **FilterFlags** de la estructura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="9f8b5-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="9f8b5-112">Marca</span><span class="sxs-lookup"><span data-stu-id="9f8b5-112">Flag</span></span>                                         | <span data-ttu-id="9f8b5-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9f8b5-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8b5-114">\_las marcas de CAPTUREFILTER \_ incluyen \_ todos los \_ SAP</span><span class="sxs-lookup"><span data-stu-id="9f8b5-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="9f8b5-115">Pasa todos los valores de SAP y notifica al controlador que todos los valores de SAP son válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="9f8b5-116">Si se combina con cualquier valor del miembro **lpSapTable** , esta marca notifica al controlador que todos los valores de SAP excepto los de **lpSapTable** son válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="9f8b5-117">\_las marcas de CAPTUREFILTER \_ incluyen \_ todos los \_ ETYPE</span><span class="sxs-lookup"><span data-stu-id="9f8b5-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="9f8b5-118">Pasa todos los valores ETYPE y notifica al controlador que todos los valores ETYPE son válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="9f8b5-119">Si se combina con cualquier valor del miembro **lpEtypeTable** , esta marca notifica al controlador que todos los valores ETYPE excepto los de **lpEtypeTable** son válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="9f8b5-120">\_marcas de \_ CAPTUREFILTER \_ solo locales</span><span class="sxs-lookup"><span data-stu-id="9f8b5-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="9f8b5-121">Al establecer esta marca, no se establecerá una NIC en modo P.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="9f8b5-122">Solo verá el tráfico local (cualquier fotograma al equipo local).</span><span class="sxs-lookup"><span data-stu-id="9f8b5-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="9f8b5-123">las \_ marcas CAPTUREFILTER \_ siguen \_ sin procesar</span><span class="sxs-lookup"><span data-stu-id="9f8b5-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="9f8b5-124">Mantiene fotogramas MAC de SMT y token ring.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="9f8b5-125">ETYPE/configuración del filtro de captura de SAP</span><span class="sxs-lookup"><span data-stu-id="9f8b5-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="9f8b5-126">Use la siguiente información para establecer los miembros **lpSapTable** y **lpEtypeTable** de la estructura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="9f8b5-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="9f8b5-127">Configuración</span><span class="sxs-lookup"><span data-stu-id="9f8b5-127">Setting</span></span>          | <span data-ttu-id="9f8b5-128">Significado</span><span class="sxs-lookup"><span data-stu-id="9f8b5-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8b5-129">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="9f8b5-129">**lpSapTable**</span></span>   | <span data-ttu-id="9f8b5-130">Muestra los valores de SAP que desea que el controlador pase.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="9f8b5-131">Esta lista indica al controlador de Monitor de red para validar cualquier marco que contenga una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="9f8b5-132">Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de todos los SAP, se convierte en una lista de excepciones (si se encuentra, no pasa).</span><span class="sxs-lookup"><span data-stu-id="9f8b5-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="9f8b5-133">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="9f8b5-133">**lpEtypeTable**</span></span> | <span data-ttu-id="9f8b5-134">Muestra los valores ETYPE que desea que pase el controlador Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="9f8b5-135">Esta lista solo indica al controlador que valide cualquier marco que contenga una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="9f8b5-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="9f8b5-136">Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de ETYPE, se convierte en una lista de excepciones (si se encuentra, no pasa).</span><span class="sxs-lookup"><span data-stu-id="9f8b5-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




