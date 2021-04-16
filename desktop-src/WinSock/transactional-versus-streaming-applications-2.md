---
description: 'Hay dos tipos fundamentales de aplicaciones de red: transaccional y de streaming. Estos tipos de aplicaciones también se denominan tipos de aplicación interactivos y de procesamiento por lotes, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Aplicaciones transaccionales frente a streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705591"
---
# <a name="transactional-versus-streaming-applications"></a><span data-ttu-id="ec2ba-104">Aplicaciones transaccionales frente a streaming</span><span class="sxs-lookup"><span data-stu-id="ec2ba-104">Transactional versus Streaming Applications</span></span>

<span data-ttu-id="ec2ba-105">Hay dos tipos fundamentales de aplicaciones de red: *transaccional* y de *streaming*.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-105">There are two fundamental types of network applications: *transactional* and *streaming*.</span></span> <span data-ttu-id="ec2ba-106">Estos tipos de aplicaciones también se denominan tipos de aplicación *interactivos* y de *procesamiento por lotes* , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-106">These application types are also called *interactive* and *batch processing* application types, respectively.</span></span>

<span data-ttu-id="ec2ba-107">Las aplicaciones transaccionales son aplicaciones STOP y go.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-107">Transactional applications are stop-and-go applications.</span></span> <span data-ttu-id="ec2ba-108">Normalmente realizan operaciones de solicitud/respuesta, que a menudo se ordenan.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-108">They usually perform request/reply operations, often ordered.</span></span> <span data-ttu-id="ec2ba-109">Algunos ejemplos de aplicaciones transaccionales son la llamada a procedimiento remoto (RPC) sincrónica, así como algunas implementaciones de HTTP y del sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="ec2ba-109">Examples of transactional applications include synchronous remote procedure call (RPC), as well as some HTTP and Domain Name System (DNS) implementations.</span></span>

<span data-ttu-id="ec2ba-110">Las aplicaciones de streaming mueven datos.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-110">Streaming applications move data.</span></span> <span data-ttu-id="ec2ba-111">Para describir las aplicaciones de streaming con un término paralelo, las aplicaciones de streaming se adhieren a una filosofía de transmisión de datos de pedal a metal, normalmente con poca preocupación para la ordenación de datos.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-111">To describe streaming applications with a parallel term, streaming applications adhere to a pedal-to-the-metal data transmission philosophy, usually with little concern for data ordering.</span></span> <span data-ttu-id="ec2ba-112">Los ejemplos de aplicaciones de streaming incluyen copia de seguridad de red y Protocolo de transferencia de archivos (FTP).</span><span class="sxs-lookup"><span data-stu-id="ec2ba-112">Examples of streaming applications include network backup and file transfer protocol (FTP).</span></span>

<span data-ttu-id="ec2ba-113">Una vez que se determina el tipo de aplicación, se determinan también sus características de red y protocolo.</span><span class="sxs-lookup"><span data-stu-id="ec2ba-113">Once the application type is determined, its network and protocol characteristics are determined as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec2ba-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec2ba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec2ba-115">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="ec2ba-115">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ec2ba-116">Dimensiones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="ec2ba-116">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



