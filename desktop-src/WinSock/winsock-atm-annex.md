---
description: ATM es aplicable a entornos de LAN y WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo de Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715470"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="a6152-103">Anexo de Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="a6152-103">Winsock ATM Annex</span></span>

<span data-ttu-id="a6152-104">ATM es aplicable a entornos de LAN y WAN.</span><span class="sxs-lookup"><span data-stu-id="a6152-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="a6152-105">Una red ATM transporta simultáneamente una amplia variedad de tráfico de red (voz, datos, imagen y vídeo).</span><span class="sxs-lookup"><span data-stu-id="a6152-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="a6152-106">Proporciona a los usuarios una calidad de servicio garantizada por canal virtual (VC).</span><span class="sxs-lookup"><span data-stu-id="a6152-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="a6152-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a6152-107">Element</span></span>          | <span data-ttu-id="a6152-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6152-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6152-109">Nombre (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="a6152-109">Protocol name(s)</span></span> | <span data-ttu-id="a6152-110">ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER</span><span class="sxs-lookup"><span data-stu-id="a6152-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="a6152-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6152-111">Description</span></span>      | <span data-ttu-id="a6152-112">ATM AAL5 proporciona un servicio de transporte que está orientado a la conexión, se conserva el límite del mensaje y se garantiza el QOS.</span><span class="sxs-lookup"><span data-stu-id="a6152-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="a6152-113">ATMPROTO \_ AALUSER es un Aal definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a6152-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="a6152-114">Familia de direcciones</span><span class="sxs-lookup"><span data-stu-id="a6152-114">Address family</span></span>   | <span data-ttu-id="a6152-115">\_ATM AF</span><span class="sxs-lookup"><span data-stu-id="a6152-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="a6152-116">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="a6152-116">Header file</span></span>      | <span data-ttu-id="a6152-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="a6152-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="a6152-118">En esta sección se describen las extensiones específicas del modo de transferencia asincrónico (ATM) necesarias para admitir los servicios ATM nativos tal y como se exponen y se especifican en la especificación de la interfaz de red de usuario (UNI) del Foro ATM versión 3. x (3,0 y 3,1).</span><span class="sxs-lookup"><span data-stu-id="a6152-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="a6152-119">Este documento admite el tipo de AAL 5 (modo de mensaje) y el AAL definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a6152-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="a6152-120">Las versiones futuras de este documento serán compatibles con otros tipos de AAL, así como de UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="a6152-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



