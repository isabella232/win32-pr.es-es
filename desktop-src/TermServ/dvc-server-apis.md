---
title: API de servidor DVC
description: Las API de servidor de canal virtual dinámico (DVC) se implementan mediante el servidor de Conexión a Escritorio remoto (RDC) de la conexión.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421286"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="bd4d8-103">API de servidor DVC</span><span class="sxs-lookup"><span data-stu-id="bd4d8-103">DVC Server APIs</span></span>

<span data-ttu-id="bd4d8-104">Las API de servidor de canal virtual dinámico (DVC) se implementan mediante el servidor de Conexión a Escritorio remoto (RDC) de la conexión.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd4d8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd4d8-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="bd4d8-106">**IWTSServerChannel**</span><span class="sxs-lookup"><span data-stu-id="bd4d8-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="bd4d8-107">No se admite esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="bd4d8-108">**IWTSServerChannelManager**</span><span class="sxs-lookup"><span data-stu-id="bd4d8-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="bd4d8-109">No se admite esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="bd4d8-110">**TPriority**</span><span class="sxs-lookup"><span data-stu-id="bd4d8-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="bd4d8-111">Esta enumeración no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="bd4d8-112">Cambios de comportamiento en otras API de servidor</span><span class="sxs-lookup"><span data-stu-id="bd4d8-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="bd4d8-113">La API de servidor se ha ampliado con una llamada adicional que abre un canal virtual dinámico (DVC).</span><span class="sxs-lookup"><span data-stu-id="bd4d8-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="bd4d8-114">La llamada adicional se realiza mediante la función [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .</span><span class="sxs-lookup"><span data-stu-id="bd4d8-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="bd4d8-115">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="bd4d8-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="bd4d8-116">Al usar esta API con DVC, siempre antepondrá los datos leídos con el [**\_ \_ encabezado de PDU de canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span><span class="sxs-lookup"><span data-stu-id="bd4d8-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="bd4d8-117">Esto significa que cualquier lectura debe realizarse con al menos el bloque de datos de **\_ \_ longitud PDU del canal** pasado como búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="bd4d8-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="bd4d8-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="bd4d8-119">Si el identificador de archivo del DVC se recupera llamando a [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con el parámetro *WTSVirtualFileHandle*, se aplicará la misma regla.</span><span class="sxs-lookup"><span data-stu-id="bd4d8-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="bd4d8-120">Todas las lecturas incluirán [**el \_ \_ encabezado de PDU de canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)y el búfer de lectura debe tener al menos el tamaño de longitud de la **\_ PDU \_ de canal** .</span><span class="sxs-lookup"><span data-stu-id="bd4d8-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 