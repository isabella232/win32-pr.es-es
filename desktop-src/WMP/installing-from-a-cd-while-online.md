---
title: Instalación desde un CD mientras está en línea
description: Instalación desde un CD mientras está en línea
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player tiendas en línea, instalar desde el CD mientras está en línea
- tiendas en línea, instalar desde el CD mientras están en línea
- Escriba 1 tiendas en línea, instalando desde el CD mientras está en línea
- Escriba 2 tiendas en línea, instalando desde el CD mientras está en línea
- Windows Media Player tiendas en línea, instalaciones en línea desde el CD
- tiendas en línea, instalaciones en línea desde el CD
- tipo 1 tiendas en línea, instalaciones en línea desde el CD
- tipo 2 tiendas en línea, instalaciones en línea desde el CD
- Windows Media Player tiendas en línea, CD se instala mientras está en línea
- tiendas en línea, CD se instala en línea
- Escriba 1 tiendas en línea, el CD se instala mientras está en línea
- tipo 2 tiendas en línea, CD se instala mientras está en línea
- instalación de tiendas en línea desde el CD en línea
- CD instala las tiendas en línea mientras están en línea
- instalaciones en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695360"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="ab99e-118">Instalación desde un CD mientras está en línea</span><span class="sxs-lookup"><span data-stu-id="ab99e-118">Installing from a CD While Online</span></span>

<span data-ttu-id="ab99e-119">Los usuarios pueden instalar Windows Media Player desde un CD mientras están conectados a Internet.</span><span class="sxs-lookup"><span data-stu-id="ab99e-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="ab99e-120">Cuando esto sucede, el programa de instalación de Windows Media Player localiza el documento ServiceInfo especificado por el parámetro de línea de comandos *ServiceInfo* .</span><span class="sxs-lookup"><span data-stu-id="ab99e-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="ab99e-121">Si el atributo **clave** coincide con el parámetro de línea de comandos *DefaultService* , el programa de instalación inspecciona el elemento de instalación para personalizar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="ab99e-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="ab99e-122">Con los valores de atributo, el programa de instalación muestra el contrato de licencia para el usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo. cab en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="ab99e-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="ab99e-123">Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="ab99e-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="ab99e-124">Una vez instalado, Windows Media Player establece la tienda en línea inicial con el nombre de clave especificado para el parámetro de línea de comandos *DefaultService* .</span><span class="sxs-lookup"><span data-stu-id="ab99e-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab99e-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab99e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab99e-126">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="ab99e-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ab99e-127">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="ab99e-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="ab99e-128">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ab99e-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="ab99e-129">**Establecimiento de la tienda en línea inicial**</span><span class="sxs-lookup"><span data-stu-id="ab99e-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="ab99e-130">**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="ab99e-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




