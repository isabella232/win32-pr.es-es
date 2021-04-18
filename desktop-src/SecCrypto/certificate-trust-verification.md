---
description: Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Comprobación de certificados de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688098"
---
# <a name="certificate-trust-verification"></a><span data-ttu-id="6b824-103">Comprobación de certificados de confianza</span><span class="sxs-lookup"><span data-stu-id="6b824-103">Certificate Trust Verification</span></span>

<span data-ttu-id="6b824-104">Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b824-104">A trust must exist between the recipient of a signed message and the signer of the message.</span></span> <span data-ttu-id="6b824-105">Un método para establecer esta confianza es a través de un [*certificado*](../secgloss/c-gly.md), un documento electrónico que comprueba que las entidades o personas son quienes dicen ser.</span><span class="sxs-lookup"><span data-stu-id="6b824-105">One method of establishing this trust is through a [*certificate*](../secgloss/c-gly.md), an electronic document verifying that entities or persons are who they claim to be.</span></span> <span data-ttu-id="6b824-106">Un tercero que confía en las dos partes de un certificado emite un certificado a una entidad.</span><span class="sxs-lookup"><span data-stu-id="6b824-106">A certificate is issued to an entity by a third party that is trusted by both of the other parties.</span></span> <span data-ttu-id="6b824-107">Por lo tanto, cada destinatario de un mensaje firmado decide si el emisor del certificado del firmante es de confianza.</span><span class="sxs-lookup"><span data-stu-id="6b824-107">So, each recipient of a signed message decides if the issuer of the signer's certificate is trustworthy.</span></span> <span data-ttu-id="6b824-108">[*CryptoAPI*](../secgloss/c-gly.md) ha implementado una metodología que permite a los desarrolladores de aplicaciones crear aplicaciones que comprueban automáticamente los certificados en una lista predefinida de certificados o [*raíces*](../secgloss/r-gly.md)de confianza.</span><span class="sxs-lookup"><span data-stu-id="6b824-108">[*CryptoAPI*](../secgloss/c-gly.md) has implemented a methodology to allow application developers to create applications that automatically verify certificates against a predefined list of trusted certificates or [*roots*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="6b824-109">Esta lista de entidades de confianza (denominadas asuntos) se denomina [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="6b824-109">This list of trusted entities (called subjects) is called a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

<span data-ttu-id="6b824-110">El siguiente ejemplo de uso de una CTL implica a un administrador de intranet (red interna) que desea controlar con qué orígenes externos son de confianza.</span><span class="sxs-lookup"><span data-stu-id="6b824-110">The following example of using a CTL involves an intranet (intra-company network) administrator who wants to control just which outside sources are trusted.</span></span> <span data-ttu-id="6b824-111">En este caso, el administrador puede crear una lista de certificados o raíces de confianza, firmarlo y hacer que la lista esté disponible para todos los clientes de la red en forma de CTL.</span><span class="sxs-lookup"><span data-stu-id="6b824-111">In this case, the administrator can create a list of trusted certificates or roots, sign it, and make the list available to all clients on the network in the form of a CTL.</span></span> <span data-ttu-id="6b824-112">Una aplicación diseñada para usar esta funcionalidad de CryptoAPI solo aceptará mensajes firmados o software descargado firmado por entidades de la lista.</span><span class="sxs-lookup"><span data-stu-id="6b824-112">An application designed to use this CryptoAPI functionality would then only accept signed messages or downloaded software that was signed by entities on the list.</span></span>

<span data-ttu-id="6b824-113">Para obtener una lista de estas funciones, consulte [funciones de comprobación de certificados](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6b824-113">For a list of these functions, see [Certificate Verification Functions](cryptography-functions.md).</span></span>

 

 
