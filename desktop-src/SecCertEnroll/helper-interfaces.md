---
description: La API de inscripción de certificados admite las siguientes interfaces de uso general.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688279"
---
# <a name="helper-interfaces"></a><span data-ttu-id="bef63-103">Interfaces auxiliares</span><span class="sxs-lookup"><span data-stu-id="bef63-103">Helper Interfaces</span></span>

<span data-ttu-id="bef63-104">La API de inscripción de certificados admite las siguientes interfaces de uso general.</span><span class="sxs-lookup"><span data-stu-id="bef63-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="bef63-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="bef63-105">Interface</span></span>                                                                    | <span data-ttu-id="bef63-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bef63-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bef63-107">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="bef63-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="bef63-108">Crea una cadena con codificación Unicode a partir de una matriz de bytes, crea una matriz de bytes a partir de una cadena codificada con Unicode y modifica el tipo de codificación Unicode que se aplica a una cadena.</span><span class="sxs-lookup"><span data-stu-id="bef63-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="bef63-109">**ICertificateAttestationChallenge**</span><span class="sxs-lookup"><span data-stu-id="bef63-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="bef63-110">Admite los desafíos de atestación de certificados.</span><span class="sxs-lookup"><span data-stu-id="bef63-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="bef63-111">**IObjectId**</span><span class="sxs-lookup"><span data-stu-id="bef63-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="bef63-112">Representa un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="bef63-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="bef63-113">**IObjectIds**</span><span class="sxs-lookup"><span data-stu-id="bef63-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="bef63-114">Administra una colección de objetos [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .</span><span class="sxs-lookup"><span data-stu-id="bef63-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="bef63-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="bef63-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="bef63-116">Representa un nombre distintivo X. 500.</span><span class="sxs-lookup"><span data-stu-id="bef63-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="bef63-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="bef63-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="bef63-118">Interfaz de clave de aprobación X. 509</span><span class="sxs-lookup"><span data-stu-id="bef63-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bef63-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bef63-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bef63-120">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="bef63-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



