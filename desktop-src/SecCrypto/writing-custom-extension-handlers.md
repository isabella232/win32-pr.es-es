---
description: Para crear extensiones personalizadas o codificar una extensión compleja, puede escribir sus propios controladores de extensión que exporten interfaces personalizadas.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Escribir controladores de extensión personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688251"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="57a26-103">Escribir controladores de extensión personalizados</span><span class="sxs-lookup"><span data-stu-id="57a26-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="57a26-104">Para crear extensiones personalizadas o codificar una extensión compleja, puede escribir sus propios controladores de extensión que exporten interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="57a26-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="57a26-105">Los servicios de Certificate Server de Microsoft se distribuyen con las siguientes interfaces que se pueden usar para codificar diversos tipos de datos de extensión: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)y [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="57a26-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="57a26-106">Estas interfaces están contenidas en Certenc.dll.</span><span class="sxs-lookup"><span data-stu-id="57a26-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="57a26-107">Además, la información de tipo de estas interfaces se incluye en Certencl.dll, que se encuentra en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="57a26-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="57a26-108">Para obtener más información sobre los controladores de extensión, vea [controladores de extensión](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="57a26-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



