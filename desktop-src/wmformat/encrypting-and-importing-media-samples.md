---
title: Cifrado e importación de ejemplos de medios
description: Cifrado e importación de ejemplos de medios
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, cifrado de ejemplos de medios
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), cifrado de muestras de medios
- DRM (administración de derechos digitales), cifrar ejemplos de medios
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, cifrado de ejemplos de medios
- API extendidas de cliente, cifrado de ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420256"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="4e975-114">Cifrado e importación de ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="4e975-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="4e975-115">Para cada ejemplo multimedia que cifre con DRM de Windows Media, debe generar un valor Salt que sea estrictamente mayor que el anterior (aumentando de forma continua).</span><span class="sxs-lookup"><span data-stu-id="4e975-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="4e975-116">Use el nuevo valor Salt para crear una clave de cifrado transitoria aplicando el algoritmo de cifrado SHA-1 al vector de inicialización concatenado con el valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4e975-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="4e975-117">A continuación, Cifre el ejemplo según el algoritmo RC4 mediante la clave transitoria generada.</span><span class="sxs-lookup"><span data-stu-id="4e975-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="4e975-118">Antes de pasar el ejemplo al SDK, la aplicación debe asociar el valor Salt al ejemplo estableciendo un atributo de extensión.</span><span class="sxs-lookup"><span data-stu-id="4e975-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="4e975-119">Estos son los pasos para cifrar ejemplos de medios:</span><span class="sxs-lookup"><span data-stu-id="4e975-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="4e975-120">Llame al método **QueryInterface** del objeto de ejemplo para obtener la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="4e975-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="4e975-121">Incremente el valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4e975-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="4e975-122">Cifre el ejemplo con un algoritmo de cifrado RC1.</span><span class="sxs-lookup"><span data-stu-id="4e975-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="4e975-123">Para el cifrado, cree una clave concatenando el vector de inicialización y el valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4e975-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="4e975-124">Proporcione el valor Salt al SDK llamando a [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="4e975-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e975-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e975-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e975-126">**Importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="4e975-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="4e975-127">**Ejemplo de cifrado de ejemplo multimedia**</span><span class="sxs-lookup"><span data-stu-id="4e975-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




