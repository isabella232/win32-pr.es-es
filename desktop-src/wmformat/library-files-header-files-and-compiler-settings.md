---
title: Archivos de biblioteca, archivos de encabezado y configuración del compilador
description: Archivos de biblioteca, archivos de encabezado y configuración del compilador
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- SDK de Windows Media Format, archivos de biblioteca DRM
- SDK de Windows Media Format, archivos de biblioteca
- SDK de Windows Media Format, archivos de encabezado DRM
- Windows Media Format SDK, archivos de encabezado
- SDK de Windows Media Format, configuración del compilador DRM
- SDK de Windows Media Format, configuración del compilador
- Administración de derechos digitales (DRM), archivos de biblioteca
- DRM (administración de derechos digitales), archivos de biblioteca
- Administración de derechos digitales (DRM), archivos de encabezado
- DRM (administración de derechos digitales), archivos de encabezado
- Administración de derechos digitales (DRM), configuración del compilador
- DRM (administración de derechos digitales), configuración del compilador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148822"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="9073f-115">Archivos de biblioteca, archivos de encabezado y configuración del compilador</span><span class="sxs-lookup"><span data-stu-id="9073f-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="9073f-116">Los componentes de programación de las API extendidas del cliente DRM de Windows Media se definen en el archivo de encabezado wmdrmsdk. h y se implementan en las bibliotecas wmdrmsdk. lib y mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9073f-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="9073f-117">Parte de la funcionalidad de las API extendidas del cliente DRM de Windows Media requiere la obtención de una biblioteca protegida de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9073f-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="9073f-118">Esta biblioteca, denominada Biblioteca de código auxiliar en esta documentación, es específica del destinatario y especifica el nivel de seguridad de la aplicación para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9073f-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="9073f-119">La biblioteca de código auxiliar reemplaza a wmdrmsdk. lib; nunca debe vincularse a ambos.</span><span class="sxs-lookup"><span data-stu-id="9073f-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="9073f-120">**Nota:** La biblioteca de código auxiliar de DRM es independiente de la biblioteca de código auxiliar usada por el resto del SDK de Windows Media Format, pero tiene licencia mediante el mismo método.</span><span class="sxs-lookup"><span data-stu-id="9073f-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="9073f-121">**Nota:** La biblioteca de rutas de DRM debe estar vinculada en la aplicación después del archivo de biblioteca msvcrt. lib para evitar errores del vinculador.</span><span class="sxs-lookup"><span data-stu-id="9073f-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="9073f-122">La biblioteca de código auxiliar contiene un certificado incrustado que Microsoft puede revocar si no cumple con los términos y condiciones del contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="9073f-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="9073f-123">Los métodos específicos que requieren la biblioteca de código auxiliar se etiquetan en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="9073f-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="9073f-124">Si intenta utilizar este tipo de método sin vincular a la biblioteca de código auxiliar, devolverá un error de STUBLIB de DRM de NS \_ E \_ DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9073f-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="9073f-125">El subsistema DRM no se puede usar en una compilación de depuración.</span><span class="sxs-lookup"><span data-stu-id="9073f-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="9073f-126">Si se intenta esto, los métodos de la API devolverán \_ el \_ error de depuración de DRM de NS E \_ \_ no \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="9073f-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9073f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9073f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9073f-128">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="9073f-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="9073f-129">**Archivos de biblioteca y configuración del compilador**</span><span class="sxs-lookup"><span data-stu-id="9073f-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="9073f-130">**Obtención de la biblioteca DRM necesaria**</span><span class="sxs-lookup"><span data-stu-id="9073f-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




