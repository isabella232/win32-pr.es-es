---
description: Los consumidores de documentos PrintCapabilities tienen ciertas obligaciones que deben cumplir para poder usar un documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de los consumidores del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec123509515de32b88c7352dcf0fc2c2b54504ff
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404948"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="069f9-103">Responsabilidades de los consumidores del documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="069f9-103">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="069f9-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="069f9-104">This topic is not current.</span></span> <span data-ttu-id="069f9-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="069f9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="069f9-106">Los consumidores de documentos PrintCapabilities tienen ciertas obligaciones que deben cumplir para poder usar un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="069f9-106">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="069f9-107">Los siguientes requisitos se aplican a los clientes de un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="069f9-107">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="069f9-108">No deben rechazar ni no procesar ningún PrintCapabilities válido sintácticamente; es decir, cualquier documento PrintCapabilities que se ajuste al esquema PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="069f9-108">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="069f9-109">Deben ser capaces de evitar la presencia inesperada o ausencia de contenido definido de forma privada.</span><span class="sxs-lookup"><span data-stu-id="069f9-109">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="069f9-110">Esto incluye contenido definido de forma privada que aparece en instancias de elementos definidos por el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="069f9-110">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="069f9-111">Deben ser capaces de evitar contenido opcional del esquema de impresión que esté ausente.</span><span class="sxs-lookup"><span data-stu-id="069f9-111">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="069f9-112">Deben tener en cuenta cuándo solicitar un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="069f9-112">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="069f9-113">Los valores de las instancias de propiedad dependen de la configuración (por lo tanto, dependientes de la instantánea).</span><span class="sxs-lookup"><span data-stu-id="069f9-113">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="069f9-114">Debe actualizar la instantánea cuando acceda a una instancia de Propiedad.</span><span class="sxs-lookup"><span data-stu-id="069f9-114">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="069f9-115">Las instancias de Feature, Option y ScoredProperty que se van a copiar en PrintTicket son estáticas por definición.</span><span class="sxs-lookup"><span data-stu-id="069f9-115">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="069f9-116">Es decir, no dependen (y no deben ser) de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="069f9-116">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="069f9-117">Si tiene acceso a cualquier instancia de estos tipos, no es necesario obtener un nuevo documento PrintCapabilities cuando cambie la configuración.</span><span class="sxs-lookup"><span data-stu-id="069f9-117">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="069f9-118">Los consumidores de PrintCapabilities que son clientes de interfaz de usuario (UI) deben poder usar la información de un documento PrintCapabilities para construir una interfaz de usuario y construir un PrintTicket válido a partir de las selecciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="069f9-118">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="069f9-119">Esto incluye saber qué instancias de ParameterInit deben especificarse y validar las instancias especificadas.</span><span class="sxs-lookup"><span data-stu-id="069f9-119">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="069f9-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="069f9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="069f9-121">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="069f9-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



