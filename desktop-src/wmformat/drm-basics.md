---
title: Aspectos básicos de DRM
description: Aspectos básicos de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- SDK de Windows Media Format, aspectos básicos de DRM
- Administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales), acerca de
- Administración de derechos digitales (DRM), protección de contenido
- DRM (administración de derechos digitales), protección de contenido
- Administración de derechos digitales (DRM), empaquetar contenido
- DRM (administración de derechos digitales), empaquetar contenido
- Administración de derechos digitales (DRM), lectura de contenido protegido
- DRM (administración de derechos digitales), lectura de contenido protegido
- protección de contenido
- empaquetado de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419137"
---
# <a name="drm-basics"></a><span data-ttu-id="0e802-114">Aspectos básicos de DRM</span><span class="sxs-lookup"><span data-stu-id="0e802-114">DRM Basics</span></span>

<span data-ttu-id="0e802-115">Las tecnologías DRM de Windows Media son bastante sencillas desde la perspectiva del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="0e802-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="0e802-116">Los componentes del SDK se pueden usar para proteger el contenido y reproducir contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="0e802-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="0e802-117">Proteger contenido</span><span class="sxs-lookup"><span data-stu-id="0e802-117">Protecting Content</span></span>

<span data-ttu-id="0e802-118">La protección del contenido (también conocido como contenido de empaquetado) implica el cifrado de la sección de datos del archivo y la inclusión de información en el encabezado del archivo que permite a los reproductores descifrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="0e802-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="0e802-119">Para cifrar el contenido, se necesita una clave, que es un valor que se usa para inicializar los algoritmos de cifrado.</span><span class="sxs-lookup"><span data-stu-id="0e802-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="0e802-120">Una clave se compone de dos partes: una inicialización de clave (o clave privada) y un identificador de clave (o clave pública).</span><span class="sxs-lookup"><span data-stu-id="0e802-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="0e802-121">La inicialización de clave es el valor secreto con el que codificará el contenido.</span><span class="sxs-lookup"><span data-stu-id="0e802-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="0e802-122">El identificador de clave es un valor público que se incluye en el encabezado de un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="0e802-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="0e802-123">Cuando un archivo está protegido, no se puede descifrar sin una licencia.</span><span class="sxs-lookup"><span data-stu-id="0e802-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="0e802-124">Una licencia incluye información que especifica las condiciones de uso para el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="0e802-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="0e802-125">El propietario del contenido decide los términos de una licencia y se puede personalizar para satisfacer diversas necesidades.</span><span class="sxs-lookup"><span data-stu-id="0e802-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="0e802-126">Parte del proceso de empaquetado de un archivo consiste en incluir la dirección URL de una página web donde los usuarios pueden adquirir una licencia para obtener acceso al contenido.</span><span class="sxs-lookup"><span data-stu-id="0e802-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="0e802-127">Lectura de contenido protegido</span><span class="sxs-lookup"><span data-stu-id="0e802-127">Reading Protected Content</span></span>

<span data-ttu-id="0e802-128">Para leer contenido protegido, debe haber una licencia para el contenido en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="0e802-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="0e802-129">Las restricciones de licencia se comprueban internamente mediante los componentes de DRM del SDK de Windows Media Format, mientras que otras deben ser aplicadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e802-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="0e802-130">Puede usar los objetos del SDK de Windows Media Format para ayudar al usuario a adquirir licencias para el contenido y realizar otras tareas administrativas, como actualizar componentes de DRM y realizar copias de seguridad de las licencias.</span><span class="sxs-lookup"><span data-stu-id="0e802-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-131">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="0e802-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0e802-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e802-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e802-133">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="0e802-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="0e802-134">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="0e802-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




