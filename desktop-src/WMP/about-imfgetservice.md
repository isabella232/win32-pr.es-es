---
title: Acerca de IMFGetService
description: Acerca de IMFGetService
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IMFGetService
- complementos, interfaz IMFGetService
- Complementos de procesamiento de señal digital, interfaz IMFGetService
- Complementos DSP, interfaz IMFGetService
- Interfaz IMFGetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356770"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="26135-113">Acerca de IMFGetService</span><span class="sxs-lookup"><span data-stu-id="26135-113">About IMFGetService</span></span>

<span data-ttu-id="26135-114">La interfaz **IMFGetService** es una de las interfaces que debe implementar un complemento DSP de modo dual.</span><span class="sxs-lookup"><span data-stu-id="26135-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="26135-115">Solo tiene un método, **GetService**.</span><span class="sxs-lookup"><span data-stu-id="26135-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="26135-116">Un complemento DSP implementa el método **GetService** para que los clientes puedan obtener punteros a las interfaces admitidas por el complemento cuando el complemento se ejecuta de forma nativa en la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="26135-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




