---
description: Referencia de comandos de COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Referencia de comandos de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677191"
---
# <a name="copp-command-reference"></a><span data-ttu-id="5beb1-103">Referencia de comandos de COPP</span><span class="sxs-lookup"><span data-stu-id="5beb1-103">COPP Command Reference</span></span>

<span data-ttu-id="5beb1-104">En esta sección se describen los comandos del Protocolo de protección de la salida (COPP).</span><span class="sxs-lookup"><span data-stu-id="5beb1-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="5beb1-105">Se definen los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="5beb1-105">The following commands are defined.</span></span>



| <span data-ttu-id="5beb1-106">Get-Help</span><span class="sxs-lookup"><span data-stu-id="5beb1-106">Command</span></span>              | <span data-ttu-id="5beb1-107">GUID</span><span class="sxs-lookup"><span data-stu-id="5beb1-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="5beb1-108">Establecer el nivel de protección</span><span class="sxs-lookup"><span data-stu-id="5beb1-108">Set Protection Level</span></span> | <span data-ttu-id="5beb1-109">**DXVA \_ COPPSetProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="5beb1-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="5beb1-110">Establecer señalización</span><span class="sxs-lookup"><span data-stu-id="5beb1-110">Set Signaling</span></span>        | <span data-ttu-id="5beb1-111">**DXVA \_ COPPSetSignaling**</span><span class="sxs-lookup"><span data-stu-id="5beb1-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="5beb1-112">Establecer nivel de protección (comando)</span><span class="sxs-lookup"><span data-stu-id="5beb1-112">Set Protection Level Command</span></span>

<span data-ttu-id="5beb1-113">Establece el nivel de protección para un mecanismo de protección de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="5beb1-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="5beb1-114">Dependiendo del conector, es posible que se pueda aplicar más de un mecanismo de protección en el mismo conector, con una configuración diferente para cada mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5beb1-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="5beb1-115">**GUID**: DXVA \_ COPPSetProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="5beb1-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="5beb1-116">**Datos de entrada**: una estructura de [**\_ COPPSetProtectionLevelCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .</span><span class="sxs-lookup"><span data-stu-id="5beb1-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="5beb1-117">Establecer comando de señalización</span><span class="sxs-lookup"><span data-stu-id="5beb1-117">Set Signaling Command</span></span>

<span data-ttu-id="5beb1-118">Especifica información sobre la señal de vídeo que no sea el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="5beb1-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="5beb1-119">En el caso de CGMS-A, determinados estándares de protección requieren que la señal televsion contenga información sobre la relación de aspecto y otra información dentro de los mismos paquetes de forma de onda de VBI que los bits de CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="5beb1-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="5beb1-120">Los televisores pueden mostrarse mal si la información de la relación de aspecto no es coherente con el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5beb1-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="5beb1-121">La aplicación puede usar este comando para especificar la relación de aspecto de modo que el controlador de gráficos pueda generar los paquetes VBI correctos.</span><span class="sxs-lookup"><span data-stu-id="5beb1-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="5beb1-122">Este comando también está diseñado para ser extensible si se requiere información de señal adicional en estándares futuros.</span><span class="sxs-lookup"><span data-stu-id="5beb1-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="5beb1-123">**GUID**: DXVA \_ COPPSetSignaling</span><span class="sxs-lookup"><span data-stu-id="5beb1-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="5beb1-124">**Datos de entrada**: una estructura de [**\_ COPPSetSignalingCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="5beb1-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5beb1-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5beb1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5beb1-126">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="5beb1-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



