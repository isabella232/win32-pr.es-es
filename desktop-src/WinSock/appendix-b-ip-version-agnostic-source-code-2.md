---
description: En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec. c y simple. c que administran correctamente el código del servidor CodeIPv6-Enabled del cliente de IPv4 o IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Apéndice B: código fuente independiente de la versión de IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907962"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="df548-103">Apéndice B: código fuente independiente de la versión de IP</span><span class="sxs-lookup"><span data-stu-id="df548-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="df548-104">En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec. c y simple. c que controla correctamente IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="df548-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="df548-105">Código de cliente habilitado para IPv6</span><span class="sxs-lookup"><span data-stu-id="df548-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="df548-106">Código de servidor habilitado para IPv6</span><span class="sxs-lookup"><span data-stu-id="df548-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="df548-107">Este código ejemplifica las directrices establecidas en esta guía de IPv6 y se incluye para proporcionar el código fuente que se ha modificado correctamente para agregar compatibilidad con IPv6.</span><span class="sxs-lookup"><span data-stu-id="df548-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="df548-108">Este ejemplo es deliberadamente sencillo, pero proporciona un ejemplo práctico para el uso y la revisión.</span><span class="sxs-lookup"><span data-stu-id="df548-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="df548-109">Una versión solo IPv4 de este código fuente se proporciona en el [Apéndice A: código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="df548-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="df548-110">Al comparar el código fuente del Apéndice A (solo IPv4) y el Apéndice B (independiente de la versión IP), se obtiene una idea de los cambios necesarios para modificar la aplicación de Windows Sockets para agregar compatibilidad con IPv6.</span><span class="sxs-lookup"><span data-stu-id="df548-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



