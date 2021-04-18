---
description: La interfaz IX509SCEPEnrollment expone los métodos siguientes.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687921"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="66740-103">Métodos IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="66740-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="66740-104">La interfaz [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="66740-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66740-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="66740-105">In this section</span></span>



| <span data-ttu-id="66740-106">Tema</span><span class="sxs-lookup"><span data-stu-id="66740-106">Topic</span></span>                                                                                                              | <span data-ttu-id="66740-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="66740-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66740-108">**Método CreateRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="66740-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="66740-109">Cree un mensaje de solicitud PKCS10 con una contraseña de desafío.</span><span class="sxs-lookup"><span data-stu-id="66740-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="66740-110">El mensaje de solicitud se encuentra en un PKCS7 con doble cifrado con el certificado de cifrado del servidor SCEP y firmado por el certificado de firma del servidor.</span><span class="sxs-lookup"><span data-stu-id="66740-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="66740-111">**Método CreateRetrieveCertificateMessage**</span><span class="sxs-lookup"><span data-stu-id="66740-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="66740-112">Recuperar un certificado emitido previamente.</span><span class="sxs-lookup"><span data-stu-id="66740-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="66740-113">**Método CreateRetrievePendingMessage**</span><span class="sxs-lookup"><span data-stu-id="66740-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="66740-114">Cree un mensaje para el sondeo de certificados (inscripción manual).</span><span class="sxs-lookup"><span data-stu-id="66740-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="66740-115">**Método DeleteRequest**</span><span class="sxs-lookup"><span data-stu-id="66740-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="66740-116">Elimine los certificados o claves creados para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66740-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="66740-117">**Initialize (método)**</span><span class="sxs-lookup"><span data-stu-id="66740-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="66740-118">Inicialice la instancia como preparación para una nueva solicitud.</span><span class="sxs-lookup"><span data-stu-id="66740-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="66740-119">**Método InitializeForPending**</span><span class="sxs-lookup"><span data-stu-id="66740-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="66740-120">Inicialice la instancia para preparar la generación de un mensaje con el fin de recuperar un certificado emitido o instalar una respuesta para una solicitud anterior del emisor.</span><span class="sxs-lookup"><span data-stu-id="66740-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="66740-121">**Método ProcessResponseMessage**</span><span class="sxs-lookup"><span data-stu-id="66740-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="66740-122">Procesa un mensaje de respuesta y devuelve la disposición del mensaje.</span><span class="sxs-lookup"><span data-stu-id="66740-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




