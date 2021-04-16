---
description: Calcular la sobrecarga con netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcular la sobrecarga con netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705657"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="a6ad5-103">Calcular la sobrecarga con netstat</span><span class="sxs-lookup"><span data-stu-id="a6ad5-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="a6ad5-104">El cálculo de la sobrecarga con netstat debe realizarse en una red silenciosa para evitar que el tráfico de red sesgado de los datos, como el tráfico de difusión o multidifusión.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="a6ad5-105">**Para calcular la sobrecarga de red de una aplicación mediante netstat**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="a6ad5-106">Recupere las estadísticas de la interfaz actual mediante netstat.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="a6ad5-107">Ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-107">Execute the application.</span></span>
3.  <span data-ttu-id="a6ad5-108">Obtenga las estadísticas de la interfaz, de nuevo mediante netstat.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="a6ad5-109">Calcule el número de bytes recibidos entre las dos medidas de netstat.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="a6ad5-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6ad5-110">Example</span></span>

<span data-ttu-id="a6ad5-111">En el ejemplo siguiente se muestran estos pasos, con TTCP para enviar 10 bytes de datos, un byte a la vez.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="a6ad5-112">En primer lugar, se calcula una sobrecarga teórica para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="a6ad5-113">Para esta prueba, todos los paquetes tienen 60 bytes (el mínimo de Ethernet).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="a6ad5-114">Esta transferencia requiere tres paquetes para configurar la conexión, 10 paquetes de datos, 10 paquetes de confirmación (la confirmación diferida se desencadena casi cada vez) y cuatro paquetes para cerrar la conexión correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="a6ad5-115">Esto equivale a 27 paquetes de 60 bytes cada uno o 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="a6ad5-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="a6ad5-116">Dado que solo se transfieren 10 bytes de datos, la sobrecarga es de 1610 bytes, que es superior al 99% de sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="a6ad5-117">Comandos:</span><span class="sxs-lookup"><span data-stu-id="a6ad5-117">Commands</span></span>

<span data-ttu-id="a6ad5-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="a6ad5-119">**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="a6ad5-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="a6ad5-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="a6ad5-121">Cálculos</span><span class="sxs-lookup"><span data-stu-id="a6ad5-121">Calculations</span></span>

<span data-ttu-id="a6ad5-122">**Enviado:** 816 bytes</span><span class="sxs-lookup"><span data-stu-id="a6ad5-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="a6ad5-123">**Recibido:** 674 bytes</span><span class="sxs-lookup"><span data-stu-id="a6ad5-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="a6ad5-124">**Total de bytes:** 1490</span><span class="sxs-lookup"><span data-stu-id="a6ad5-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="a6ad5-125">**Bytes de usuario:** 10</span><span class="sxs-lookup"><span data-stu-id="a6ad5-125">**User bytes:** 10</span></span>

<span data-ttu-id="a6ad5-126">**Sobrecarga:** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="a6ad5-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="a6ad5-127">\* \* Goodput: \* \* = 5 bytes/segundo (o 40 bits/s)</span><span class="sxs-lookup"><span data-stu-id="a6ad5-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="a6ad5-128">Los bytes reales transferidos no coinciden con los valores teóricos debido a que no se tienen en cuenta los bytes de relleno en los valores de netstat.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a6ad5-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6ad5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6ad5-130">Comportamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a6ad5-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="a6ad5-131">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="a6ad5-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



