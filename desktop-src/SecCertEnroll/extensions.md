---
description: El formato de certificado X. 509 versión 3 identifica varias extensiones que se pueden agregar a un certificado.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensiones (API de inscripción de certificados)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648525"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="bf435-103">Extensiones (API de inscripción de certificados)</span><span class="sxs-lookup"><span data-stu-id="bf435-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="bf435-104">El formato de certificado X. 509 versión 3 identifica varias extensiones que se pueden agregar a un certificado.</span><span class="sxs-lookup"><span data-stu-id="bf435-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="bf435-105">Las extensiones proporcionan información mejorada sobre el uso de claves, las directivas de certificados y las restricciones, los formularios de nombres alternativos, etc.</span><span class="sxs-lookup"><span data-stu-id="bf435-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="bf435-106">Puede usar la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir un valor de extensión.</span><span class="sxs-lookup"><span data-stu-id="bf435-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="bf435-107">Muchas de las extensiones comunes se pueden crear mediante el uso de interfaces predefinidas derivadas de **IX509Extension**.</span><span class="sxs-lookup"><span data-stu-id="bf435-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="bf435-108">Se agrega una colección de extensiones a una solicitud de certificado incluyendo la colección en los atributos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf435-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="bf435-109">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf435-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="bf435-110">Extensiones admitidas</span><span class="sxs-lookup"><span data-stu-id="bf435-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="bf435-111">\#Extensiones PKCS 10</span><span class="sxs-lookup"><span data-stu-id="bf435-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="bf435-112">Extensiones de CMC</span><span class="sxs-lookup"><span data-stu-id="bf435-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



