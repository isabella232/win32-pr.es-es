---
description: Los protocolos de Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001850"
---
# <a name="schannel-credentials"></a><span data-ttu-id="846f6-103">Credenciales de Schannel</span><span class="sxs-lookup"><span data-stu-id="846f6-103">Schannel Credentials</span></span>

<span data-ttu-id="846f6-104">Los protocolos de Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes.</span><span class="sxs-lookup"><span data-stu-id="846f6-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="846f6-105">La autenticación de servidor, donde el servidor proporciona la prueba de su identidad al cliente, es necesaria para los [*protocolos de seguridad*](../secgloss/s-gly.md)de Schannel.</span><span class="sxs-lookup"><span data-stu-id="846f6-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="846f6-106">El servidor puede solicitar la autenticación de cliente en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="846f6-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="846f6-107">Las credenciales de Schannel son certificados [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="846f6-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="846f6-108">La información de clave [*pública*](../secgloss/p-gly.md) y [*privada*](../secgloss/p-gly.md) de los certificados se usa para autenticar el servidor y, opcionalmente, el cliente.</span><span class="sxs-lookup"><span data-stu-id="846f6-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="846f6-109">Estas claves también se usan para proporcionar [*integridad*](../secgloss/i-gly.md) del mensaje, mientras que el cliente y el servidor intercambian la información necesaria para generar e intercambiar [*claves de sesión*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="846f6-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="846f6-110">Para obtener información de programación, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="846f6-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
