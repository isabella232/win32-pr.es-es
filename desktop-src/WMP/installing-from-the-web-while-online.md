---
title: Instalación desde la web en línea
description: Instalación desde la web en línea
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player tiendas en línea, instalar desde web mientras está en línea
- tiendas en línea, instalar desde web en línea
- Escriba 1 tiendas en línea, instalación desde web mientras está en línea
- Escriba 2 tiendas en línea, instalación desde web mientras está en línea
- Windows Media Player tiendas en línea, instalaciones en línea desde web
- tiendas en línea, instalaciones en línea desde web
- tipo 1 tiendas en línea, instalaciones en línea desde web
- tipo 2 tiendas en línea, instalaciones en línea desde web
- instalación de tiendas en línea desde web en línea
- instalaciones en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685568"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="f4b9a-113">Instalación desde la web en línea</span><span class="sxs-lookup"><span data-stu-id="f4b9a-113">Installing from the Web While Online</span></span>

<span data-ttu-id="f4b9a-114">Los usuarios pueden instalar Windows Media Player como una descarga web mientras están conectados a Internet.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="f4b9a-115">En este caso, Microsoft puede configurar la tienda en línea inicial que especifique.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="f4b9a-116">Para redistribuir Windows Media Player de esta manera, use la siguiente dirección URL:</span><span class="sxs-lookup"><span data-stu-id="f4b9a-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="f4b9a-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*versión*&UserLocale =*localID*&servicio =*clave*</span><span class="sxs-lookup"><span data-stu-id="f4b9a-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="f4b9a-118">En la dirección URL anterior, establezca *clave* en el nombre de la clave de la tienda en línea y establezca *localeID* en el identificador de la configuración regional en la que el almacén proporciona el servicio.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="f4b9a-119">Establezca *versión* en 2 para Windows Media Player 11 en Windows XP o 1 para Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="f4b9a-120">La dirección URL instala Windows Media Player y establece el almacén activo inicial en el especificado por *clave*.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="f4b9a-121">En el ejemplo siguiente se muestra una dirección URL que instala Windows Media Player 11 y establece Proseware como el almacén activo inicial.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="f4b9a-122">El valor de 409 para *localeID* indica que Proseware proporciona el servicio en el Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="f4b9a-123">Si el documento ServiceInfo de la tienda en línea incluye un elemento install, el programa de instalación de Windows Media Player personalizará el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="f4b9a-124">Con los valores de atributo, el programa de instalación muestra el contrato de licencia para el usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo. cab en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="f4b9a-125">Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f4b9a-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4b9a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4b9a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b9a-127">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="f4b9a-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f4b9a-128">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="f4b9a-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="f4b9a-129">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f4b9a-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="f4b9a-130">**Establecimiento de la tienda en línea inicial**</span><span class="sxs-lookup"><span data-stu-id="f4b9a-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




