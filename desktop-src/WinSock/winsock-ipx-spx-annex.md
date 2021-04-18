---
description: En esta sección se describen las extensiones de Winsock específicas del intercambio de paquetes de interconexión/intercambio de paquetes secuenciados (IPX/SPX). También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden exhibir un comportamiento único.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de Winsock IPX/SPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705885"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="53fae-104">Anexo de Winsock IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="53fae-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="53fae-105">En esta sección se describen las extensiones de Winsock específicas del intercambio de paquetes de interconexión/intercambio de paquetes secuenciados (IPX/SPX).</span><span class="sxs-lookup"><span data-stu-id="53fae-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="53fae-106">También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden exhibir un comportamiento único.</span><span class="sxs-lookup"><span data-stu-id="53fae-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="53fae-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="53fae-107">Element</span></span>          | <span data-ttu-id="53fae-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="53fae-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53fae-109">Nombre (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="53fae-109">Protocol name(s)</span></span> | <span data-ttu-id="53fae-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="53fae-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="53fae-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="53fae-111">Description</span></span>      | <span data-ttu-id="53fae-112">Proporciona servicios de transporte a través de la capa de red IPX: IPX para datagramas no confiables, SPX para flujos de mensajes confiables y orientados a la conexión.</span><span class="sxs-lookup"><span data-stu-id="53fae-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="53fae-113">Familia de direcciones</span><span class="sxs-lookup"><span data-stu-id="53fae-113">Address family</span></span>   | <span data-ttu-id="53fae-114">AF \_ IPX</span><span class="sxs-lookup"><span data-stu-id="53fae-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="53fae-115">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="53fae-115">Header file</span></span>      | <span data-ttu-id="53fae-116">WSIPX. h</span><span class="sxs-lookup"><span data-stu-id="53fae-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="53fae-117">En esta sección se describe cómo usar WinSock con la familia de protocolos de IPX, lo que permite migrar las aplicaciones de IPX tradicionales a Winsock.</span><span class="sxs-lookup"><span data-stu-id="53fae-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="53fae-118">Las redes IPX funcionan de manera fundamentalmente diferente que las redes IP, por lo que se deben tener en cuenta tales diferencias al usar IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="53fae-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



