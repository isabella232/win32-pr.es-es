---
description: La interfaz IX509SCEPEnrollment expone las siguientes propiedades.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Propiedades de IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687920"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="17864-103">Propiedades de IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="17864-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="17864-104">La interfaz [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="17864-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="17864-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="17864-105">In this section</span></span>



| <span data-ttu-id="17864-106">Tema</span><span class="sxs-lookup"><span data-stu-id="17864-106">Topic</span></span>                                                                                              | <span data-ttu-id="17864-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="17864-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17864-108">**Propiedad de certificado**</span><span class="sxs-lookup"><span data-stu-id="17864-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="17864-109">Obtiene el certificado para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="17864-110">**Propiedad CertificateFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="17864-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="17864-111">Obtiene o establece el nombre descriptivo del certificado.</span><span class="sxs-lookup"><span data-stu-id="17864-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="17864-112">**Propiedad FailInfo**</span><span class="sxs-lookup"><span data-stu-id="17864-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="17864-113">Obtiene información cuando el método [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) detecta un entorno con errores.</span><span class="sxs-lookup"><span data-stu-id="17864-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="17864-114">**Propiedad OldCertificate**</span><span class="sxs-lookup"><span data-stu-id="17864-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="17864-115">Obtiene o establece un certificado antiguo que se va a reemplazar por una solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="17864-116">**Propiedad request**</span><span class="sxs-lookup"><span data-stu-id="17864-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="17864-117">Obtiene la solicitud interna de PKCS10.</span><span class="sxs-lookup"><span data-stu-id="17864-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="17864-118">**Propiedad ServerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="17864-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="17864-119">Establece los algoritmos hash y de cifrado preferidos para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="17864-120">**Propiedad SignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="17864-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="17864-121">Obtiene o establece el certificado del firmante para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="17864-122">**Propiedad Silent**</span><span class="sxs-lookup"><span data-stu-id="17864-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="17864-123">Obtiene o establece si se va a permitir la interfaz de usuario durante la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="17864-124">**Propiedad Status**</span><span class="sxs-lookup"><span data-stu-id="17864-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="17864-125">Obtiene el estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="17864-126">**Propiedad TransactionId**</span><span class="sxs-lookup"><span data-stu-id="17864-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="17864-127">Obtiene o establece el identificador de transacción de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17864-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




