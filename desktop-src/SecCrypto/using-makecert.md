---
description: Use los comandos MakeCert para crear certificados de prueba con las opciones disponibles con la versión 4,0 o posterior de Internet Explorer.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso de MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811234"
---
# <a name="using-makecert"></a><span data-ttu-id="f70b1-103">Uso de MakeCert</span><span class="sxs-lookup"><span data-stu-id="f70b1-103">Using MakeCert</span></span>

<span data-ttu-id="f70b1-104">En los ejemplos siguientes se usan comandos [Makecert](makecert.md) para crear certificados de prueba mediante las opciones disponibles con Internet Explorer versión 4,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f70b1-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="f70b1-105">Cree un certificado emitido por la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="f70b1-106">Guarde el certificado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f70b1-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="f70b1-107">**Makecert** *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="f70b1-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="f70b1-108">Cree un certificado emitido por la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="f70b1-109">Guárdelo en un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="f70b1-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="f70b1-110">**Makecert-SS** *MyNewStore*</span><span class="sxs-lookup"><span data-stu-id="f70b1-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="f70b1-111">Cree un certificado emitido por la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="f70b1-112">Cree un contenedor de claves y guarde el certificado en un almacén y en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f70b1-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="f70b1-113">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="f70b1-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="f70b1-114">Cree un certificado emitido por la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="f70b1-115">Cree un archivo de clave privada y guarde el certificado en un almacén y en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f70b1-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="f70b1-116">**Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="f70b1-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="f70b1-117">Cree un certificado emitido por la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="f70b1-118">Cree un contenedor de claves, guarde el certificado en un almacén y un archivo, y haga que la clave privada se pueda exportar.</span><span class="sxs-lookup"><span data-stu-id="f70b1-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="f70b1-119">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**</span><span class="sxs-lookup"><span data-stu-id="f70b1-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="f70b1-120">Cree un certificado mediante la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="f70b1-121">Guarde el certificado en un almacén.</span><span class="sxs-lookup"><span data-stu-id="f70b1-121">Save the certificate to a store.</span></span> <span data-ttu-id="f70b1-122">A continuación, cree otro certificado emitido por el certificado recién creado.</span><span class="sxs-lookup"><span data-stu-id="f70b1-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="f70b1-123">Guarde el segundo certificado en otro almacén.</span><span class="sxs-lookup"><span data-stu-id="f70b1-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="f70b1-124">**Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="f70b1-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="f70b1-125">Cree un certificado mediante la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="f70b1-126">Guarde el certificado en mi almacén.</span><span class="sxs-lookup"><span data-stu-id="f70b1-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="f70b1-127">A continuación, cree otro certificado mediante el certificado recién creado.</span><span class="sxs-lookup"><span data-stu-id="f70b1-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="f70b1-128">Si hay más de un certificado en el almacén MY, el certificado se debe identificar mediante su nombre común.</span><span class="sxs-lookup"><span data-stu-id="f70b1-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="f70b1-129">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My Makecert-is My-in "XXZZYY"-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="f70b1-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="f70b1-130">Cree un certificado mediante la raíz de prueba predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f70b1-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="f70b1-131">Guarde el certificado en el almacén MY y en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f70b1-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="f70b1-132">A continuación, cree otro certificado mediante el certificado *MyNew* recién creado.</span><span class="sxs-lookup"><span data-stu-id="f70b1-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="f70b1-133">Si hay más de un certificado en el almacén MY, identifique de forma única el primer certificado con el nombre de archivo del certificado.</span><span class="sxs-lookup"><span data-stu-id="f70b1-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="f70b1-134">**Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is My-IC** *MyNew. cer* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="f70b1-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



