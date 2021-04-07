---
description: No se puede predecir fácilmente el futuro de las comunicaciones seguras y criptográficas.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Extender la funcionalidad de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002914"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="f3e08-103">Extender la funcionalidad de CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="f3e08-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="f3e08-104">No se puede predecir fácilmente el futuro de las comunicaciones seguras y [*criptográficas*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e08-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="f3e08-105">Pueden surgir nuevos tipos de certificados, varias extensiones de certificado pueden encontrar un uso común y se pueden introducir nuevos tipos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3e08-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="f3e08-106">Debido a esto, la extensibilidad es parte del diseño de las funciones clave de [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e08-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="f3e08-107">Las secciones siguientes presentan información general sobre el uso de OID para extender las funciones de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f3e08-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="f3e08-108">Tema</span><span class="sxs-lookup"><span data-stu-id="f3e08-108">Topic</span></span>                                                                              | <span data-ttu-id="f3e08-109">Contenido</span><span class="sxs-lookup"><span data-stu-id="f3e08-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3e08-110">Información general sobre OID</span><span class="sxs-lookup"><span data-stu-id="f3e08-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="f3e08-111">Conceptos fundamentales de OID.</span><span class="sxs-lookup"><span data-stu-id="f3e08-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="f3e08-112">Crear la nueva funcionalidad</span><span class="sxs-lookup"><span data-stu-id="f3e08-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="f3e08-113">Crear OID y funciones para extender el uso de las API existentes.</span><span class="sxs-lookup"><span data-stu-id="f3e08-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="f3e08-114">Registrar la nueva funcionalidad</span><span class="sxs-lookup"><span data-stu-id="f3e08-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="f3e08-115">Configurar nuevas funciones relacionadas con OID.</span><span class="sxs-lookup"><span data-stu-id="f3e08-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="f3e08-116">Instalación de la nueva funcionalidad</span><span class="sxs-lookup"><span data-stu-id="f3e08-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="f3e08-117">Instalación de funciones OID en la memoria para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f3e08-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="f3e08-118">Extensión de la funcionalidad de CertOpenStore</span><span class="sxs-lookup"><span data-stu-id="f3e08-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="f3e08-119">Extensión de la funcionalidad de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) mediante la función de proveedor de almacén de certificados instalable o registrada.</span><span class="sxs-lookup"><span data-stu-id="f3e08-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
