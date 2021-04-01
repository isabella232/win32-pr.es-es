---
title: Parámetros de la línea de comandos del programa de instalación para tiendas en línea
description: Parámetros de la línea de comandos del programa de instalación para tiendas en línea
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player tiendas en línea, parámetros de la línea de comandos del programa de instalación
- tiendas en línea, parámetros de la línea de comandos del programa de instalación
- Escriba 1 tiendas en línea, parámetros de la línea de comandos del programa de instalación
- tipo 2 tiendas en línea, parámetros de la línea de comandos del programa de instalación
- parámetros de la línea de comandos del programa de instalación
- Windows Media Player tiendas en línea, parámetros de la línea de comandos
- tiendas en línea, parámetros de la línea de comandos
- tipo 1 almacenes en línea, parámetros de la línea de comandos
- tipo 2 tiendas en línea, parámetros de la línea de comandos
- parámetros de la línea de comandos
- Windows Media Player tiendas en línea, parámetros
- tiendas en línea, parámetros
- tipo 1 tiendas en línea, parámetros
- tipo 2 tiendas en línea, parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075655"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="d919c-117">Parámetros de la línea de comandos del programa de instalación para tiendas en línea</span><span class="sxs-lookup"><span data-stu-id="d919c-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="d919c-118">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="d919c-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d919c-119">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d919c-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d919c-120">Al instalar Windows Media Player 10 o Windows Media Player 11 en Windows XP, puede anexar parámetros de la línea de comandos para especificar la primera tienda en línea que el usuario ve.</span><span class="sxs-lookup"><span data-stu-id="d919c-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="d919c-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d919c-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="d919c-122">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d919c-122">Parameters</span></span>

<span data-ttu-id="d919c-123">DefaultService (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="d919c-123">DefaultService (required)</span></span>

<span data-ttu-id="d919c-124">Nombre de clave de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d919c-124">The key name for the online store.</span></span> <span data-ttu-id="d919c-125">Este valor debe coincidir con el nombre de clave del atributo **clave** del elemento **ServiceInfo** del documento serviceinfo.</span><span class="sxs-lookup"><span data-stu-id="d919c-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="d919c-126">ServiceInfo (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="d919c-126">ServiceInfo (required)</span></span>

<span data-ttu-id="d919c-127">La ruta de acceso completa a un documento ServiceInfo instalado en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="d919c-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="d919c-128">ServiceExtra (opcional)</span><span class="sxs-lookup"><span data-stu-id="d919c-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="d919c-129">Cadena de consulta que Windows Media Player 10 anexará a la dirección URL del documento ServiceInfo cuando recupere el documento en línea.</span><span class="sxs-lookup"><span data-stu-id="d919c-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="d919c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d919c-130">Remarks</span></span>

<span data-ttu-id="d919c-131">Para obtener más información acerca de cómo redistribuir el software de Windows Media Player con su aplicación, consulte [redistribuir el software de windows media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="d919c-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="d919c-132">Cuando el equipo del usuario no está conectado a Internet, la información contenida en el documento ServiceInfo local se usa para configurar Windows Media Player para el servicio activo inicial.</span><span class="sxs-lookup"><span data-stu-id="d919c-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="d919c-133">Los parámetros de línea de comandos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d919c-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d919c-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d919c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d919c-135">**Tiendas en línea con personalización de marca**</span><span class="sxs-lookup"><span data-stu-id="d919c-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d919c-136">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="d919c-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d919c-137">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="d919c-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="d919c-138">**Establecimiento de la tienda en línea inicial**</span><span class="sxs-lookup"><span data-stu-id="d919c-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




