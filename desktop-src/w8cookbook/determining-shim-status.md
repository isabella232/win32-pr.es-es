---
title: Determinar el estado de la corrección de compatibilidad
description: Determinar el estado de la corrección de compatibilidad
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357535"
---
# <a name="determining-shim-status"></a><span data-ttu-id="b3e9a-103">Determinar el estado de la corrección de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="b3e9a-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="b3e9a-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="b3e9a-104">Platforms</span></span>

<dl> <span data-ttu-id="b3e9a-105">Clientes: Windows 8</span><span class="sxs-lookup"><span data-stu-id="b3e9a-105">Clients - Windows 8</span></span>  
<span data-ttu-id="b3e9a-106">Servidores: Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3e9a-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="b3e9a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3e9a-107">Description</span></span>

<span data-ttu-id="b3e9a-108">Windows 8 registra eventos cuando las aplicaciones se corregido por varias razones.</span><span class="sxs-lookup"><span data-stu-id="b3e9a-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="b3e9a-109">La forma más fácil de determinar si la aplicación se está corregido es comprobar el visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="b3e9a-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="b3e9a-110">Vaya a registros de aplicaciones y servicios \\ Microsoft Windows Application-Experience \\ telemetría de programas.</span><span class="sxs-lookup"><span data-stu-id="b3e9a-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b3e9a-111">Mitigación</span><span class="sxs-lookup"><span data-stu-id="b3e9a-111">Mitigation</span></span>

<span data-ttu-id="b3e9a-112">La mejor manera de obtener acceso a SHIMMING es cambiar el nombre del archivo ejecutable o aumentar la versión principal en 1 (volver a compilar el archivo ejecutable).</span><span class="sxs-lookup"><span data-stu-id="b3e9a-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




