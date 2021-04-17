---
description: Cada Windows Installer característica usa uno o varios componentes Windows Installer, y las características pueden compartir componentes.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Especificar relaciones Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677432"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="726db-103">Especificar relaciones Feature-Component</span><span class="sxs-lookup"><span data-stu-id="726db-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="726db-104">Cada [Windows Installer característica](windows-installer-features.md) usa uno o varios [componentes Windows Installer](windows-installer-components.md), y las características pueden compartir componentes.</span><span class="sxs-lookup"><span data-stu-id="726db-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="726db-105">La [tabla FeatureComponents](featurecomponents-table.md) define la relación entre las características y los componentes de.</span><span class="sxs-lookup"><span data-stu-id="726db-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="726db-106">Vea el [grupo de tablas principales](core-tables-group.md) y [los componentes y características](components-and-features.md) en la información general de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="726db-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="726db-107">En esta sección, agregará información a la tabla FeatureComponents del ejemplo de Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="726db-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="726db-108">Use el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla FeatureComponents vacía.</span><span class="sxs-lookup"><span data-stu-id="726db-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="726db-109">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="726db-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="726db-110">Característica\_</span><span class="sxs-lookup"><span data-stu-id="726db-110">Feature\_</span></span> | <span data-ttu-id="726db-111">Componente\_</span><span class="sxs-lookup"><span data-stu-id="726db-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="726db-112">Baloncesto</span><span class="sxs-lookup"><span data-stu-id="726db-112">Baseball</span></span>  | <span data-ttu-id="726db-113">Baloncesto</span><span class="sxs-lookup"><span data-stu-id="726db-113">Baseball</span></span>    |
| <span data-ttu-id="726db-114">Concierto</span><span class="sxs-lookup"><span data-stu-id="726db-114">Concert</span></span>   | <span data-ttu-id="726db-115">Concierto</span><span class="sxs-lookup"><span data-stu-id="726db-115">Concert</span></span>     |
| <span data-ttu-id="726db-116">Dance</span><span class="sxs-lookup"><span data-stu-id="726db-116">Dance</span></span>     | <span data-ttu-id="726db-117">Dance</span><span class="sxs-lookup"><span data-stu-id="726db-117">Dance</span></span>       |
| <span data-ttu-id="726db-118">Balón</span><span class="sxs-lookup"><span data-stu-id="726db-118">Football</span></span>  | <span data-ttu-id="726db-119">Balón</span><span class="sxs-lookup"><span data-stu-id="726db-119">Football</span></span>    |
| <span data-ttu-id="726db-120">Ayuda</span><span class="sxs-lookup"><span data-stu-id="726db-120">Help</span></span>      | <span data-ttu-id="726db-121">Ayuda</span><span class="sxs-lookup"><span data-stu-id="726db-121">Help</span></span>        |
| <span data-ttu-id="726db-122">January</span><span class="sxs-lookup"><span data-stu-id="726db-122">January</span></span>   | <span data-ttu-id="726db-123">January</span><span class="sxs-lookup"><span data-stu-id="726db-123">January</span></span>     |
| <span data-ttu-id="726db-124">NewYears</span><span class="sxs-lookup"><span data-stu-id="726db-124">NewYears</span></span>  | <span data-ttu-id="726db-125">NewYears</span><span class="sxs-lookup"><span data-stu-id="726db-125">NewYears</span></span>    |
| <span data-ttu-id="726db-126">Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="726db-126">Notepad</span></span>   | <span data-ttu-id="726db-127">Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="726db-127">Notepad</span></span>     |
| <span data-ttu-id="726db-128">Léame</span><span class="sxs-lookup"><span data-stu-id="726db-128">Readme</span></span>    | <span data-ttu-id="726db-129">Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="726db-129">Notepad</span></span>     |



 

[<span data-ttu-id="726db-130">Continuar</span><span class="sxs-lookup"><span data-stu-id="726db-130">Continue</span></span>](adding-registry-information.md)

 

 



