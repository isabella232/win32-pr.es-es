---
title: Establecimiento de la tienda en línea inicial
description: Establecimiento de la tienda en línea inicial
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Windows Media Player tiendas en línea, configurar las tiendas en línea iniciales
- tiendas en línea, configurar las tiendas en línea iniciales
- Escriba 1 tiendas en línea, estableciendo las tiendas en línea iniciales
- Escriba 2 tiendas en línea y establezca las tiendas en línea iniciales
- Windows Media Player tiendas en línea, visualización de la primera tienda en línea
- tiendas en línea, primera tienda en línea visualizada
- tipo 1 tiendas en línea, vista primera tienda en línea
- tipo 2 tiendas en línea, vista primera tienda en línea
- primera tienda en línea visualizada
- establecimiento de las tiendas en línea iniciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903698"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="fafc8-113">Establecimiento de la tienda en línea inicial</span><span class="sxs-lookup"><span data-stu-id="fafc8-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="fafc8-114">Para obtener más información acerca de cómo redistribuir el software de Windows Media Player con su aplicación, consulte [redistribuir el software de windows media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="fafc8-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="fafc8-115">Cuando un usuario instala primero Windows Media Player, la aplicación de instalación establece la tienda en línea activa inicial en un valor predeterminado elegido por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fafc8-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="fafc8-116">Los fabricantes de equipos originales (OEM) de equipos personales pueden optar por cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="fafc8-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="fafc8-117">Para especificar y configurar la primera tienda en línea que el usuario ve cuando instala Windows Media Player, debe:</span><span class="sxs-lookup"><span data-stu-id="fafc8-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="fafc8-118">Cree un documento ServiceInfo que instale en el disco duro del usuario.</span><span class="sxs-lookup"><span data-stu-id="fafc8-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="fafc8-119">Este documento contiene información acerca de cómo configurar la tienda en línea activa inicial.</span><span class="sxs-lookup"><span data-stu-id="fafc8-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="fafc8-120">Anexe un conjunto de parámetros de línea de comandos al ejecutar la aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="fafc8-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="fafc8-121">Existen tres escenarios para instalar Windows Media Player y establecer la tienda en línea inicial.</span><span class="sxs-lookup"><span data-stu-id="fafc8-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="fafc8-122">En las secciones siguientes se proporcionan más detalles sobre cada escenario:</span><span class="sxs-lookup"><span data-stu-id="fafc8-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="fafc8-123">Instalación sin conexión</span><span class="sxs-lookup"><span data-stu-id="fafc8-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="fafc8-124">Instalación desde un CD mientras está en línea</span><span class="sxs-lookup"><span data-stu-id="fafc8-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="fafc8-125">Instalación desde la web en línea</span><span class="sxs-lookup"><span data-stu-id="fafc8-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="fafc8-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fafc8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fafc8-127">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="fafc8-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fafc8-128">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fafc8-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="fafc8-129">**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="fafc8-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




