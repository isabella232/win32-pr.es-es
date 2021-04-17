---
description: La sintaxis de mensajes criptográficos (CMS), derivada de PKCS \# 7 versión 1,5, es la sintaxis que se usa para el hash, firma digital, autenticación y cifrado de mensajes arbitrarios.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Adiciones de CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666825"
---
# <a name="cms-additions"></a><span data-ttu-id="edf3f-103">Adiciones de CMS</span><span class="sxs-lookup"><span data-stu-id="edf3f-103">CMS Additions</span></span>

<span data-ttu-id="edf3f-104">La sintaxis de mensajes criptográficos (CMS), derivada de PKCS \# 7 versión 1,5, es la sintaxis que se usa para el [*hash*](../secgloss/h-gly.md), [*firma digital*](../secgloss/d-gly.md), autenticación y cifrado de mensajes arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="edf3f-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="edf3f-105">Siempre que sea posible, se conserva la compatibilidad con versiones anteriores. sin embargo, se han realizado cambios para acomodar las técnicas de transferencia de certificados y de acuerdo de claves para la administración de claves.</span><span class="sxs-lookup"><span data-stu-id="edf3f-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="edf3f-106">CMS permite la encapsulación múltiple para que se pueda anidar un sobre de encapsulación dentro de otro.</span><span class="sxs-lookup"><span data-stu-id="edf3f-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="edf3f-107">Además, una parte puede firmar digitalmente los datos encapsulados previamente; los atributos arbitrarios, como el tiempo de firma, se pueden firmar junto con el contenido del mensaje. los atributos y, como las [*Contrafirmas*](../secgloss/c-gly.md), se pueden asociar a una firma.</span><span class="sxs-lookup"><span data-stu-id="edf3f-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="edf3f-108">CMS puede admitir una variedad de arquitecturas para la administración de claves basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="edf3f-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="edf3f-109">Para admitir capacidades adicionales de CMS, se han asignado nuevos campos a las estructuras de datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="edf3f-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="edf3f-110">También se han agregado nuevas marcas y valores de parámetro.</span><span class="sxs-lookup"><span data-stu-id="edf3f-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="edf3f-111">Todas las estructuras de datos y todas las API que usan CMS tienen un 100% de compatibilidad con versiones anteriores con PKCS \# 7, versión 1,5.</span><span class="sxs-lookup"><span data-stu-id="edf3f-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="edf3f-112">Las adiciones incluyen [adiciones de datos con envoltorio](enveloped-data-additions.md) y [adiciones de datos firmados](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="edf3f-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
