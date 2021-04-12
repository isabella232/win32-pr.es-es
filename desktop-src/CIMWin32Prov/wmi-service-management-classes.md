---
description: Las clases de administración de servicios WMI se utilizan para administrar el propio servicio WMI, no el sistema informático o la red empresarial. La administración de WMI abarca tanto la configuración del servicio WMI como la administración de las operaciones de WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Clases de administración de servicios WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152852"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="e0cdb-104">Clases de administración de servicios WMI</span><span class="sxs-lookup"><span data-stu-id="e0cdb-104">WMI Service Management Classes</span></span>

<span data-ttu-id="e0cdb-105">Las clases de administración de servicios WMI se utilizan para administrar el propio servicio WMI, no el sistema informático o la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="e0cdb-106">La administración de WMI abarca tanto la configuración del servicio WMI como la administración de las operaciones de WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="e0cdb-107">La categoría administración de servicios WMI incluye las siguientes subcategorías de clases:</span><span class="sxs-lookup"><span data-stu-id="e0cdb-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="e0cdb-108">Clases de configuración de WMI</span><span class="sxs-lookup"><span data-stu-id="e0cdb-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="e0cdb-109">Clases de administración de WMI</span><span class="sxs-lookup"><span data-stu-id="e0cdb-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="e0cdb-110">Clases de configuración de WMI</span><span class="sxs-lookup"><span data-stu-id="e0cdb-110">WMI Configuration Classes</span></span>

<span data-ttu-id="e0cdb-111">La clase de configuración WMI deriva métodos que configuran el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="e0cdb-112">La siguiente es una tabla de clases de configuración de WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="e0cdb-113">Clase</span><span class="sxs-lookup"><span data-stu-id="e0cdb-113">Class</span></span>                                                             | <span data-ttu-id="e0cdb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0cdb-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="e0cdb-115">**Win32 \_ MethodParameterClass**</span><span class="sxs-lookup"><span data-stu-id="e0cdb-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="e0cdb-116">Clase base abstracta que implementa los parámetros de método derivados de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="e0cdb-117">Clases de administración de WMI</span><span class="sxs-lookup"><span data-stu-id="e0cdb-117">WMI Management Classes</span></span>

<span data-ttu-id="e0cdb-118">Las clases de administración de WMI representan parámetros operativos para el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="e0cdb-119">La siguiente es una tabla de clases de administración de WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="e0cdb-120">Clase</span><span class="sxs-lookup"><span data-stu-id="e0cdb-120">Class</span></span>                                                       | <span data-ttu-id="e0cdb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0cdb-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0cdb-122">**Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="e0cdb-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="e0cdb-123">Contiene los parámetros operativos para el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="e0cdb-124">**Win32 \_ WMIElementSetting**</span><span class="sxs-lookup"><span data-stu-id="e0cdb-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="e0cdb-125">Asociación entre un servicio que se ejecuta en el sistema de Windows y la configuración de WMI que puede usar.</span><span class="sxs-lookup"><span data-stu-id="e0cdb-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e0cdb-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0cdb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0cdb-127">Clases Win32</span><span class="sxs-lookup"><span data-stu-id="e0cdb-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
