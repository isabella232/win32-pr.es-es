---
title: Guía de programación para las tiendas en línea de tipo 1
description: Guía de programación para las tiendas en línea de tipo 1
ms.assetid: 6950cab8-4355-4699-8245-f2817c3e25fc
keywords:
- Windows Media Player tiendas en línea, guía de programación
- tiendas en línea, guía de programación
- tipo 1 almacenes en línea, guía de programación
- Guía de programación, tipo 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea04cb188a68c85173b5b1682235b6964840d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269185"
---
# <a name="programming-guide-for-type-1-online-stores"></a><span data-ttu-id="3b193-107">Guía de programación para las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="3b193-107">Programming Guide for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="3b193-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="3b193-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3b193-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3b193-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3b193-110">Esta sección contiene los temas siguientes para ayudarle a crear una tienda en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="3b193-110">This section contains the following topics to help you create a type 1 online store.</span></span>



| <span data-ttu-id="3b193-111">Sección</span><span class="sxs-lookup"><span data-stu-id="3b193-111">Section</span></span>                                                                                                              | <span data-ttu-id="3b193-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b193-112">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b193-113">Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="3b193-113">Example ServiceInfo Document for a Type 1 Online Store</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="3b193-114">Muestra un documento de ServiceInfo de ejemplo que puede usar como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="3b193-114">Shows an example ServiceInfo document that you can use as a starting point.</span></span>                                                                    |
| [<span data-ttu-id="3b193-115">Compilar el complemento para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="3b193-115">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)                 | <span data-ttu-id="3b193-116">Explica cómo crear el complemento necesario para una tienda en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="3b193-116">Explains how to build the required plug-in for a type 1 online store.</span></span>                                                                          |
| [<span data-ttu-id="3b193-117">Mostrar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="3b193-117">Displaying Dialog Boxes</span></span>](displaying-dialog-boxes.md)                                                               | <span data-ttu-id="3b193-118">Explica cómo invocar los cuadros de diálogo a través de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="3b193-118">Explains how to invoke dialog boxes through Windows Media Player.</span></span>                                                                              |
| [<span data-ttu-id="3b193-119">Administrar inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="3b193-119">Managing Login</span></span>](managing-login.md)                                                                                 | <span data-ttu-id="3b193-120">Explica cómo interactuar con Windows Media Player elementos de la interfaz de usuario que permiten a los usuarios iniciar sesión en y cerrar sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3b193-120">Explains how to interact with Windows Media Player user interface elements that let users log in to and log out from the online store.</span></span>         |
| [<span data-ttu-id="3b193-121">Compra de contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="3b193-121">Purchasing Media Content</span></span>](purchasing-media-content.md)                                                             | <span data-ttu-id="3b193-122">Explica cómo interactúan Windows Media Player y el complemento de la tienda en línea cuando el usuario adquiere contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b193-122">Explains how Windows Media Player and the online store's plug-in interact when the user purchases media content.</span></span>                               |
| [<span data-ttu-id="3b193-123">Descargar contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="3b193-123">Downloading Media Content</span></span>](downloading-media-content.md)                                                           | <span data-ttu-id="3b193-124">Explica cómo interactúan Windows Media Player y el complemento de la tienda en línea cuando el usuario descarga contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b193-124">Explains how Windows Media Player and the online store's plug-in interact when the user downloads media content.</span></span>                               |
| [<span data-ttu-id="3b193-125">Actualización de licencias</span><span class="sxs-lookup"><span data-stu-id="3b193-125">Updating Licenses</span></span>](updating-licenses.md)                                                                           | <span data-ttu-id="3b193-126">Explica cómo interactúan Windows Media Player y el complemento de la tienda en línea para mantener actualizadas las licencias multimedia del usuario.</span><span class="sxs-lookup"><span data-stu-id="3b193-126">Explains how Windows Media Player and the online store's plug-in interact to keep the user's media licenses current.</span></span>                           |
| [<span data-ttu-id="3b193-127">Actualización de dispositivos portátiles</span><span class="sxs-lookup"><span data-stu-id="3b193-127">Updating Portable Devices</span></span>](updating-portable-devices.md)                                                           | <span data-ttu-id="3b193-128">Explica cómo interactúan Windows Media Player y el complemento de la tienda en línea cuando el contenido multimedia se mueve entre el equipo y un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="3b193-128">Explains how Windows Media Player and the online store's plug-in interact when media content moves between the computer and a portable device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3b193-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b193-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b193-130">**Tipo 1 tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="3b193-130">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




