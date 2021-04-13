---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tipo 2 tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359086"
---
# <a name="bits"></a><span data-ttu-id="2400a-108">BITS</span><span class="sxs-lookup"><span data-stu-id="2400a-108">BITS</span></span>

<span data-ttu-id="2400a-109">El [servicio de transferencia inteligente en segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) es una característica del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2400a-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="2400a-110">BITS transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información de progreso relacionada con las transferencias.</span><span class="sxs-lookup"><span data-stu-id="2400a-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="2400a-111">Si desea transferir archivos mediante código de C++, BITS es la tecnología correcta que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2400a-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="2400a-112">Si desea transferir archivos mediante código JScript en la Página Web de la tienda en línea, use el administrador de descargas en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2400a-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="2400a-113">Dado que el administrador de descargas de Windows Media Player usa BITS, puede realizar los pasos necesarios para configurar los trabajos de copia de BITS de forma que Windows Media Player administre los trabajos.</span><span class="sxs-lookup"><span data-stu-id="2400a-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="2400a-114">Para ello, debe seguir la Convención descrita en la sección [Convención de trabajo de Windows Media Player bits](windows-media-player-bits-job-convention.md) al agregar los trabajos a la cola de transferencia de bits.</span><span class="sxs-lookup"><span data-stu-id="2400a-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="2400a-115">En esta sección también se describe un mecanismo para recuperar información sobre los trabajos de BITS de la Página Web de tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="2400a-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2400a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2400a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2400a-117">**Uso del administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="2400a-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="2400a-118">**Acerca de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="2400a-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 