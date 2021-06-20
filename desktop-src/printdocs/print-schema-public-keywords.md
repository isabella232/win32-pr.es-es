---
description: En este artículo se especifican las palabras clave públicas que se definen para el esquema de impresión y su uso para PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Palabras clave públicas del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407148"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="85e66-103">Palabras clave públicas del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="85e66-103">Print Schema Public Keywords</span></span>

<span data-ttu-id="85e66-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="85e66-104">This topic is not current.</span></span> <span data-ttu-id="85e66-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85e66-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85e66-106">En la sección siguiente se especifican las palabras clave públicas que se definen para el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="85e66-106">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="85e66-107">Uso de palabras clave públicas de esquema de impresión para funcionalidades de impresión</span><span class="sxs-lookup"><span data-stu-id="85e66-107">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="85e66-108">Las palabras clave especificadas en PrintCapabilities Public Keywords (Palabras clave públicas de PrintCapabilities) PUEDEN aparecer en un documento De capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="85e66-108">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="85e66-109">Para obtener más información sobre cómo interactúan estas palabras clave con la tecnología PrintCapabilities, consulte Información general [de la sección PrintCapabilities.](overview-of-the-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="85e66-109">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="85e66-110">Las palabras clave públicas específicas de PrintTicket NO DEBERÍAN aparecer en un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="85e66-110">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="85e66-111">Uso de palabras clave públicas de esquema de impresión para PrintTicket</span><span class="sxs-lookup"><span data-stu-id="85e66-111">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="85e66-112">Las palabras clave especificadas en PrintTicket Public Keywords (Palabras clave públicas de PrintTicket) PUEDEN aparecer en printTicket.</span><span class="sxs-lookup"><span data-stu-id="85e66-112">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="85e66-113">Las palabras clave PrintTicket se implementan como un tipo de elemento Property.</span><span class="sxs-lookup"><span data-stu-id="85e66-113">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="85e66-114">Para obtener más información sobre cómo interactúan estas palabras clave con la tecnología PrintTicket, consulte la sección Información de configuración no relacionada [con PrintCapabilities.](configuration-information-not-related-to-printcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="85e66-114">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="85e66-115">Las palabras clave especificadas en PrintCapabilities Public Keywords (Palabras clave públicas de PrintCapabilities) PUEDEN aparecer en printTicket en función de la implementación de PrintTicket en una aplicación o controlador.</span><span class="sxs-lookup"><span data-stu-id="85e66-115">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="85e66-116">Esto proporciona selecciones para los atributos de dispositivo definidos en el documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="85e66-116">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="85e66-117">Para obtener más información sobre la interacción entre las palabras clave PrintCapabilities y PrintTicket, consulte [Propósito de la sección PrintTicket.](purpose-of-the-printticket.md)</span><span class="sxs-lookup"><span data-stu-id="85e66-117">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85e66-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85e66-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e66-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="85e66-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



