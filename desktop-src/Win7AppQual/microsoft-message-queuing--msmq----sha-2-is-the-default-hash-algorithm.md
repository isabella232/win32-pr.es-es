---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088103"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="69df6-103">Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado</span><span class="sxs-lookup"><span data-stu-id="69df6-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="69df6-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="69df6-104">Affected Platforms</span></span>

 <span data-ttu-id="69df6-105">**Clientes:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="69df6-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="69df6-106">**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69df6-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="69df6-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="69df6-107">Feature Impact</span></span>

 <span data-ttu-id="69df6-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="69df6-108">**Severity** - Low</span></span>  
<span data-ttu-id="69df6-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="69df6-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="69df6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="69df6-110">Description</span></span>

<span data-ttu-id="69df6-111">En Windows 7, MSMQ usa SHA-2 como valor predeterminado al firmar un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="69df6-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="69df6-112">Además, todos los mensajes entrantes deben estar firmados con SHA-2.</span><span class="sxs-lookup"><span data-stu-id="69df6-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="69df6-113">Puede habilitar la compatibilidad con un algoritmo de cifrado inferior a través de una clave del Registro accesible para el administrador.</span><span class="sxs-lookup"><span data-stu-id="69df6-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="69df6-114">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="69df6-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="69df6-115">MSMQ en Windows 2003 o una versión inferior no aceptará mensajes firmados que se origine en MSMQ en Windows 7</span><span class="sxs-lookup"><span data-stu-id="69df6-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="69df6-116">MSMQ en Windows 7 no aceptará mensajes firmados procedentes de Windows 2008 o inferiores</span><span class="sxs-lookup"><span data-stu-id="69df6-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="69df6-117">Mitigación</span><span class="sxs-lookup"><span data-stu-id="69df6-117">Mitigation</span></span>

<span data-ttu-id="69df6-118">Los usuarios deben considerar la posibilidad de actualizar a Windows 7 para aprovechar el algoritmo de firma más seguro.</span><span class="sxs-lookup"><span data-stu-id="69df6-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="69df6-119">Para habilitar el intercambio de mensajes firmados sin problemas entre Windows 7 y cualquier sistema operativo de nivel inferior, el administrador debe agregar las excepciones adecuadas en los equipos MSMQ.</span><span class="sxs-lookup"><span data-stu-id="69df6-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



