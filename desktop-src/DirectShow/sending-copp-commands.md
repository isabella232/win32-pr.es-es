---
description: Envío de comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Envío de comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677089"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="799e3-103">Envío de comandos COPP</span><span class="sxs-lookup"><span data-stu-id="799e3-103">Sending COPP Commands</span></span>

<span data-ttu-id="799e3-104">Para enviar un comando de protocolo de protección de la salida (COPP) certificado, rellene una estructura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="799e3-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="799e3-105">**guidCommandID**.</span><span class="sxs-lookup"><span data-stu-id="799e3-105">**guidCommandID**.</span></span> <span data-ttu-id="799e3-106">GUID que identifica el comando.</span><span class="sxs-lookup"><span data-stu-id="799e3-106">The GUID that identifies the command.</span></span> <span data-ttu-id="799e3-107">Consulte la referencia de comandos de COPP.</span><span class="sxs-lookup"><span data-stu-id="799e3-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="799e3-108">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="799e3-108">**dwSequence**.</span></span> <span data-ttu-id="799e3-109">Número de secuencia del comando.</span><span class="sxs-lookup"><span data-stu-id="799e3-109">The command sequence number.</span></span> <span data-ttu-id="799e3-110">Incremente este valor después de cada comando.</span><span class="sxs-lookup"><span data-stu-id="799e3-110">Increment this value after each command.</span></span> <span data-ttu-id="799e3-111">(Este valor se muestra como **uCommandSeq** en [el inicio de una sesión de COPP](initiating-a-copp-session.md)).</span><span class="sxs-lookup"><span data-stu-id="799e3-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="799e3-112">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="799e3-112">**cbSizeData**.</span></span> <span data-ttu-id="799e3-113">Tamaño, en bytes, de los datos necesarios para el comando.</span><span class="sxs-lookup"><span data-stu-id="799e3-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="799e3-114">**CommandData**.</span><span class="sxs-lookup"><span data-stu-id="799e3-114">**CommandData**.</span></span> <span data-ttu-id="799e3-115">Datos para el comando.</span><span class="sxs-lookup"><span data-stu-id="799e3-115">Data for the command.</span></span>

<span data-ttu-id="799e3-116">Una vez que haya rellenado los datos, calcule el equipo MAC para el comando:</span><span class="sxs-lookup"><span data-stu-id="799e3-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="799e3-117">Calcule la etiqueta OMAC-1 para el bloque de datos que aparece después del miembro **macKDI** de la estructura **AMCOPPCommand** .</span><span class="sxs-lookup"><span data-stu-id="799e3-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="799e3-118">Copie este valor en el miembro **macKDI** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="799e3-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="799e3-119">Pase ahora la estructura al método [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .</span><span class="sxs-lookup"><span data-stu-id="799e3-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="799e3-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="799e3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="799e3-121">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="799e3-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



