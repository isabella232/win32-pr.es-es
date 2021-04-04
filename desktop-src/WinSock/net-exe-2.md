---
description: Net.exe se puede usar para detener e iniciar el protocolo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907942"
---
# <a name="netexe"></a><span data-ttu-id="e915f-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="e915f-103">Net.exe</span></span>

<span data-ttu-id="e915f-104">Net.exe se puede usar para detener e iniciar el protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e915f-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="e915f-105">Al reiniciar IPv6, se reinicializa el protocolo como si el equipo se reiniciara, lo que puede cambiar los números de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e915f-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="e915f-106">Net.exe tiene muchos subcomandos.</span><span class="sxs-lookup"><span data-stu-id="e915f-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="e915f-107">Los siguientes comandos son relevantes para IPv6:</span><span class="sxs-lookup"><span data-stu-id="e915f-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="e915f-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span><span class="sxs-lookup"><span data-stu-id="e915f-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="e915f-109">Detiene el protocolo IPv6 y lo descarga de la memoria.</span><span class="sxs-lookup"><span data-stu-id="e915f-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="e915f-110">Este comando genera un error si hay Sockets IPv6 abiertos.</span><span class="sxs-lookup"><span data-stu-id="e915f-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="e915f-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span><span class="sxs-lookup"><span data-stu-id="e915f-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="e915f-112">Inicia el protocolo IPv6 si se detuvo.</span><span class="sxs-lookup"><span data-stu-id="e915f-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="e915f-113">Si hay un nuevo archivo de controlador de Tcpip6.sys en el directorio% SystemRoot% \\ system32 \\ drivers, se carga ese archivo de controlador.</span><span class="sxs-lookup"><span data-stu-id="e915f-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



