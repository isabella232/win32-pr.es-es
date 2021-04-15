---
description: Muchas de las funciones requieren tipos de codificación de mensajes o de certificados.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificación de mensajes y certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497273"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="546be-103">Tipos de codificación de mensajes y certificados</span><span class="sxs-lookup"><span data-stu-id="546be-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="546be-104">Muchas de las funciones requieren tipos de [*codificación de mensajes*](../secgloss/m-gly.md)o de certificados.</span><span class="sxs-lookup"><span data-stu-id="546be-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="546be-105">Este tipo de codificación es un **valor DWORD**, que posiblemente contiene los tipos de codificación de mensajes y de certificado.</span><span class="sxs-lookup"><span data-stu-id="546be-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="546be-106">El tipo de codificación del certificado se almacena en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="546be-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="546be-107">El tipo de codificación del mensaje se almacena en la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="546be-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="546be-108">Algunas funciones o campos de estructura requieren solo uno de los tipos de codificación, pero siempre es aceptable especificar ambos tipos de codificación.</span><span class="sxs-lookup"><span data-stu-id="546be-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="546be-109">Para obtener un ejemplo en el que se especifican ambos tipos de codificación, vea [ \# includes y \# defines](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="546be-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="546be-110">La siguiente Convención de nomenclatura de parámetros se usa para indicar los tipos de codificación necesarios.</span><span class="sxs-lookup"><span data-stu-id="546be-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="546be-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="546be-111">Name</span></span>                       | <span data-ttu-id="546be-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="546be-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="546be-113">*dwMsgAndCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="546be-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="546be-114">Ambos tipos de codificación son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="546be-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="546be-115">*dwMsgEncodingType*</span><span class="sxs-lookup"><span data-stu-id="546be-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="546be-116">Solo se requiere el tipo de codificación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="546be-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="546be-117">*dwCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="546be-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="546be-118">Solo se requiere el tipo de codificación de certificado.</span><span class="sxs-lookup"><span data-stu-id="546be-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="546be-119">*dwEncodingType*</span><span class="sxs-lookup"><span data-stu-id="546be-119">*dwEncodingType*</span></span>           | <span data-ttu-id="546be-120">Se requiere un mensaje o un tipo de codificación de certificado.</span><span class="sxs-lookup"><span data-stu-id="546be-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="546be-121">Si la palabra de orden inferior que contiene el tipo de codificación de certificado es distinto de cero, se usa.</span><span class="sxs-lookup"><span data-stu-id="546be-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="546be-122">De lo contrario, se usa la palabra de orden superior que contiene el tipo de codificación de mensajes.</span><span class="sxs-lookup"><span data-stu-id="546be-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="546be-123">Si se especifican ambos, se usa el tipo de codificación del certificado en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="546be-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="546be-124">En la tabla siguiente se muestran los tipos de codificación definidos actualmente.</span><span class="sxs-lookup"><span data-stu-id="546be-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="546be-125">Tipo de codificación</span><span class="sxs-lookup"><span data-stu-id="546be-125">Encoding type</span></span>          | <span data-ttu-id="546be-126">Value</span><span class="sxs-lookup"><span data-stu-id="546be-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="546be-127">CIFRAdo de la \_ \_ codificación ASN</span><span class="sxs-lookup"><span data-stu-id="546be-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="546be-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="546be-128">0x00000001</span></span> |
| <span data-ttu-id="546be-129">\_Codificación ASN de X509 \_</span><span class="sxs-lookup"><span data-stu-id="546be-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="546be-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="546be-130">0x00000001</span></span> |
| <span data-ttu-id="546be-131">CODIFICACIÓN de ASN de PKCS \_ 7 \_ \_</span><span class="sxs-lookup"><span data-stu-id="546be-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="546be-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="546be-132">0x00010000</span></span> |



 

 

 
