---
description: Un usuario puede comprobar el estado de la interfaz Teredo desde el símbolo del sistema escribiendo netsh interface Teredo show State y examinando la salida.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: La infraestructura del mismo nivel y Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545518"
---
# <a name="the-peer-infrastructure-and-teredo"></a><span data-ttu-id="5a29a-103">La infraestructura del mismo nivel y Teredo</span><span class="sxs-lookup"><span data-stu-id="5a29a-103">The Peer Infrastructure and Teredo</span></span>

<span data-ttu-id="5a29a-104">Un usuario puede comprobar el estado de la interfaz [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) desde el símbolo del sistema escribiendo **netsh interface Teredo show State** y examinando la salida.</span><span class="sxs-lookup"><span data-stu-id="5a29a-104">A user can check the status of the [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) interface from the command prompt by typing **netsh interface teredo show state** and examining the output.</span></span> <span data-ttu-id="5a29a-105">Si el estado es "sin conexión", Teredo no está activo, lo que impide que el usuario se conecte a otros usuarios a través de sus direcciones Teredo.</span><span class="sxs-lookup"><span data-stu-id="5a29a-105">If the state is "offline", Teredo is not active, which prevents the user from connecting to other users via their Teredo addresses.</span></span> <span data-ttu-id="5a29a-106">Es posible que Teredo esté sin conexión porque el Firewall está deshabilitado o no es compatible con [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="5a29a-106">It is possible Teredo may be offline because your firewall is disabled or does not support [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span></span>

 

 
