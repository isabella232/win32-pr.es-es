---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de los consumidores del documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717417"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="c8b67-104">Responsabilidades de los consumidores del documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c8b67-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="c8b67-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c8b67-105">This topic is not current.</span></span> <span data-ttu-id="c8b67-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c8b67-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c8b67-107">Los consumidores de documentos de PrintCapabilities tienen ciertas obligaciones que deben mantener antes de poder usar un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c8b67-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="c8b67-108">Los siguientes requisitos se aplican a los clientes de un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c8b67-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="c8b67-109">No deben rechazar o no procesar ninguna PrintCapabilities válida sintácticamente. es decir, cualquier documento de PrintCapabilities que se ajuste al esquema de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c8b67-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="c8b67-110">Deben ser capaces de solucionar la presencia inesperada o la ausencia de contenido definido de forma privada.</span><span class="sxs-lookup"><span data-stu-id="c8b67-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="c8b67-111">Esto incluye contenido definido de forma privada que aparece dentro de las instancias de los elementos definidos por el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="c8b67-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="c8b67-112">Deben ser capaces de solucionar el contenido opcional del esquema de impresión que falta.</span><span class="sxs-lookup"><span data-stu-id="c8b67-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="c8b67-113">Deben tener en cuenta cuándo solicitar un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="c8b67-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="c8b67-114">Los valores de las instancias de propiedades dependen de la configuración (por tanto, dependen de la instantánea).</span><span class="sxs-lookup"><span data-stu-id="c8b67-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="c8b67-115">Debe actualizar la instantánea cuando tenga acceso a una instancia de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c8b67-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="c8b67-116">Las instancias de Feature, Option y ScoredProperty que se van a copiar en un PrintTicket son por definición static.</span><span class="sxs-lookup"><span data-stu-id="c8b67-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="c8b67-117">Es decir, no son (y no deben ser) en función de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8b67-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="c8b67-118">Si obtiene acceso a cualquier instancia de estos tipos, no es necesario obtener un nuevo documento de PrintCapabilities cuando cambia la configuración.</span><span class="sxs-lookup"><span data-stu-id="c8b67-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="c8b67-119">Los consumidores de PrintCapabilities que son clientes de interfaz de usuario (IU) deben poder usar la información de un documento de PrintCapabilities para construir una interfaz de usuario y para construir un PrintTicket válido a partir de las selecciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8b67-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="c8b67-120">Esto incluye saber qué instancias de ParameterInit se deben especificar y validar las instancias especificadas.</span><span class="sxs-lookup"><span data-stu-id="c8b67-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8b67-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8b67-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8b67-122">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c8b67-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



