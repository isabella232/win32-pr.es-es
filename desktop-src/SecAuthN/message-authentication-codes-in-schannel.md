---
description: Un código de autentificación de mensajes (MAC) (MAC) se usa para detectar la alteración y falsificación de mensajes.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticación de mensajes en Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278130"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="e0286-103">Códigos de autenticación de mensajes en Schannel</span><span class="sxs-lookup"><span data-stu-id="e0286-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="e0286-104">Un [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac) se usa para detectar la alteración y falsificación de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e0286-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="e0286-105">El remitente de un mensaje crea un equipo MAC mediante el cifrado de un [*hash*](../secgloss/h-gly.md) unidireccional del cuerpo del mensaje mediante una [*clave de sesión*](../secgloss/s-gly.md) compartida por el remitente y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="e0286-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="e0286-106">El equipo MAC se anexa al mensaje que se envía al destinatario.</span><span class="sxs-lookup"><span data-stu-id="e0286-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="e0286-107">El destinatario del mensaje vuelve a generar el equipo MAC, con la clave de sesión compartida y el cuerpo del mensaje, y compara el equipo MAC generado con el equipo MAC recibido del remitente.</span><span class="sxs-lookup"><span data-stu-id="e0286-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="e0286-108">Si los dos son idénticos, el remitente debe tener la clave de sesión compartida y el mensaje no se ha modificado en tránsito.</span><span class="sxs-lookup"><span data-stu-id="e0286-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="e0286-109">En los protocolos Schannel, el algoritmo utilizado para generar el equipo MAC viene determinado por el [conjunto de cifrado](cipher-suites-in-schannel.md) que usa el remitente y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="e0286-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
