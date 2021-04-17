---
description: Enumera los cambios en las capacidades para la protección de datos.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adiciones de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666949"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="190f9-103">Adiciones de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="190f9-103">Enveloped Data Additions</span></span>

<span data-ttu-id="190f9-104">Se han realizado los siguientes cambios en las capacidades de datos con doble cifrado:</span><span class="sxs-lookup"><span data-stu-id="190f9-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="190f9-105">La identificación de destinatarios solo puede realizarse mediante el emisor y el número de serie (PKCS \# 7 1,5), pero también con el identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="190f9-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="190f9-106">Se proporcionan tres opciones de intercambio de claves de destinatario:</span><span class="sxs-lookup"><span data-stu-id="190f9-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="190f9-107">Transporte de claves mediante claves RSA.</span><span class="sxs-lookup"><span data-stu-id="190f9-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="190f9-108">Acuerdo de claves mediante Ephemeral-Static Diffie-Hellman las claves de algoritmo encapsuladas con 3DES o RC2, o Ephemeral-Static las claves de algoritmo Diffie-Hellman de curva elíptica encapsuladas con AES.</span><span class="sxs-lookup"><span data-stu-id="190f9-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="190f9-109">Clave de cifrado de claves o transferencia de clave de lista de correo en la que la clave usada para cifrar la clave de cifrado de contenido ya se ha distribuido a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="190f9-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="190f9-110">RC2, 3DES y AES se permiten como algoritmos de ajuste de clave.</span><span class="sxs-lookup"><span data-stu-id="190f9-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="190f9-111">Los atributos no protegidos pueden incluirse en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="190f9-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="190f9-112">Se ha agregado un campo **OriginatorInfo** que contiene información sobre el originador que puede contener certificados y CRL.</span><span class="sxs-lookup"><span data-stu-id="190f9-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="190f9-113">Los algoritmos basados en criptografía de curva elíptica (ECC) y AES requieren Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="190f9-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



