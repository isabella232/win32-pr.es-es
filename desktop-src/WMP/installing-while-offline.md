---
title: Instalación sin conexión
description: Instalación sin conexión
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player tiendas en línea, instalación sin conexión
- tiendas en línea, instalar sin conexión
- tipo 1 almacenes en línea, instalación sin conexión
- tipo 2 tiendas en línea, instalación sin conexión
- Windows Media Player tiendas en línea, instalaciones sin conexión
- tiendas en línea, instalaciones sin conexión
- tipo 1 tiendas en línea, instalaciones sin conexión
- tipo 2 tiendas en línea, instalaciones sin conexión
- instalación de tiendas en línea sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903584"
---
# <a name="installing-while-offline"></a><span data-ttu-id="eb4f8-112">Instalación sin conexión</span><span class="sxs-lookup"><span data-stu-id="eb4f8-112">Installing While Offline</span></span>

<span data-ttu-id="eb4f8-113">Los usuarios pueden instalar Windows Media Player mientras no están conectados a Internet.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="eb4f8-114">Cuando esto sucede, el programa de instalación de Windows Media Player localiza el ServiceInfo.xml documento especificado por el parámetro de línea de comandos *ServiceInfo* .</span><span class="sxs-lookup"><span data-stu-id="eb4f8-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="eb4f8-115">Si el atributo **clave** coincide con el parámetro de línea de comandos *DefaultService* , el programa de instalación aplica la información de los siguientes elementos a Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="eb4f8-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="eb4f8-116">FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-116">FriendlyName.</span></span> <span data-ttu-id="eb4f8-117">El nombre descriptivo de la tienda en línea se muestra en la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="eb4f8-118">Color.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-118">Color.</span></span> <span data-ttu-id="eb4f8-119">Los colores especificados se aplican a la barra de tareas y los botones.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="eb4f8-120">ServiceTask1, ServiceTask2 y ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="eb4f8-121">Se establecen los elementos secundarios ButtonText y ButtonTip.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="eb4f8-122">No se ha establecido el atributo URL.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-122">The URL attribute is not set.</span></span> <span data-ttu-id="eb4f8-123">La dirección URL se establece una vez que el usuario se conecta a Internet y Windows Media Player recupera su lista de tiendas en línea de manera normal.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="eb4f8-124">Imagen.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-124">Image.</span></span> <span data-ttu-id="eb4f8-125">Se establecen los atributos MenuURL y ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="eb4f8-126">Estas direcciones URL deben apuntar a las imágenes instaladas en el disco duro del usuario mediante el protocolo file://.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="eb4f8-127">Cuando el usuario intenta ver la tienda en línea, Windows Media Player muestra un mensaje que informa al usuario de que se requiere una conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="eb4f8-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb4f8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb4f8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb4f8-129">**Elemento color**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-130">**Elemento FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-131">**Elemento Image**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-132">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-133">**ServiceInfo, elemento**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-134">**Elemento ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-135">**Elemento ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-136">**Elemento ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-137">**Establecimiento de la tienda en línea inicial**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="eb4f8-138">**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="eb4f8-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




