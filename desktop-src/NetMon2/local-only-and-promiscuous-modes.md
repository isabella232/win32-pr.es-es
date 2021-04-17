---
description: Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modos Local-Only e promiscuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666546"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="e1ad5-103">Modos Local-Only e promiscuo</span><span class="sxs-lookup"><span data-stu-id="e1ad5-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="e1ad5-104">Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="e1ad5-105">En el modo de solo local, el proveedor de paquetes de red (NPP) devuelve los fotogramas que se envían al equipo en el que se ejecuta el monitor, incluidas las difusiones y multidifusión dirigidas a la máquina local.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="e1ad5-106">Aunque se limita a los marcos dirigidos localmente, el modo local también es mucho menos procesador.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="e1ad5-107">En el modo promiscuo, el monitor también puede ver el tráfico que no se dirige a o desde el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="e1ad5-108">A menos que el monitor haya especificado la marca, MCS \_ Create \_ PMODE \_ no \_ es necesario, en la función [OnLoadingDLL](onloadingdll.md) , el servicio de control de supervisión (MCSVC) supone que el monitor requiere el modo promiscuo cuando carga el archivo DLL del monitor.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



