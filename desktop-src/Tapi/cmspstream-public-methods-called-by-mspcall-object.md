---
description: La lista siguiente contiene los métodos CMSPStream llamados por el objeto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Métodos CMSPStream llamados por el objeto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687890"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="191be-103">CMSPStream métodos públicos llamados por el objeto MSPCall</span><span class="sxs-lookup"><span data-stu-id="191be-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="191be-104">Métodos públicos de CMSPStream</span><span class="sxs-lookup"><span data-stu-id="191be-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="191be-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="191be-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="191be-106">**Smss**</span><span class="sxs-lookup"><span data-stu-id="191be-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="191be-107">Lo llama **MSPCall** cuando se crea la secuencia.</span><span class="sxs-lookup"><span data-stu-id="191be-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="191be-108">**Apagado**</span><span class="sxs-lookup"><span data-stu-id="191be-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="191be-109">Lo llama **MSPCall** para anular la selección de todos los objetos de terminal y liberar el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="191be-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="191be-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="191be-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="191be-111">Lo llama el objeto MSPCall para obtener el estado actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="191be-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="191be-112">**HandleTSPData**</span><span class="sxs-lookup"><span data-stu-id="191be-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="191be-113">El objeto de llamada derivado puede llamar a este método para permitir que la secuencia controle los comandos de TSP.</span><span class="sxs-lookup"><span data-stu-id="191be-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="191be-114">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="191be-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="191be-115">Lo llama el objeto MSPCall para permitir que el flujo Controle los eventos de gráfico.</span><span class="sxs-lookup"><span data-stu-id="191be-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



