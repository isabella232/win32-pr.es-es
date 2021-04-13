---
title: VCM (arquitectura)
description: VCM (arquitectura)
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo para Windows (VFW), arquitectura VCM
- VFW (vídeo para Windows), VCM Architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357367"
---
# <a name="vcm-architecture"></a><span data-ttu-id="89fe4-105">VCM (arquitectura)</span><span class="sxs-lookup"><span data-stu-id="89fe4-105">VCM Architecture</span></span>

<span data-ttu-id="89fe4-106">VCM es un intermediario entre una aplicación y controladores de compresión y descompresión.</span><span class="sxs-lookup"><span data-stu-id="89fe4-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="89fe4-107">Los controladores de compresión y descompresión comprimen y descomprimen tramas de datos individuales.</span><span class="sxs-lookup"><span data-stu-id="89fe4-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="89fe4-108">Cuando una aplicación realiza una llamada a VCM, VCM traduce la llamada en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="89fe4-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="89fe4-109">El mensaje se envía mediante la función [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al compresor o descompresor adecuado, que comprime o descomprime los datos.</span><span class="sxs-lookup"><span data-stu-id="89fe4-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="89fe4-110">VCM recibe el valor devuelto del controlador de compresión o descompresión y, a continuación, devuelve el control a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89fe4-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="89fe4-111">Si se define una macro para un mensaje, la macro se expande a una llamada de función **ICSendMessage** que proporciona los parámetros adecuados para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="89fe4-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="89fe4-112">Si se define una macro para un mensaje, la aplicación debe utilizarla en lugar del mensaje.</span><span class="sxs-lookup"><span data-stu-id="89fe4-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="89fe4-113">En esta información general, estas macros siguen los mensajes entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="89fe4-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




