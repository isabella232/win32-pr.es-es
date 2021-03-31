---
title: Consultar dispositivos de audio auxiliares
description: Consultar dispositivos de audio auxiliares
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio de onda, consulta de dispositivos de audio auxiliares
- audio auxiliar, consultar dispositivos
- interfaz de audio auxiliar
- dispositivos de audio auxiliares, consulta
- consultar dispositivos de audio auxiliares
- audio auxiliar, interfaz
- audio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077633"
---
# <a name="querying-auxiliary-audio-devices"></a><span data-ttu-id="52587-110">Consultar dispositivos de audio auxiliares</span><span class="sxs-lookup"><span data-stu-id="52587-110">Querying Auxiliary Audio Devices</span></span>

<span data-ttu-id="52587-111">No todos los sistemas multimedia tienen soporte de audio auxiliar.</span><span class="sxs-lookup"><span data-stu-id="52587-111">Not all multimedia systems have auxiliary audio support.</span></span> <span data-ttu-id="52587-112">Puede usar la función [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) para determinar el número de dispositivos auxiliares que se pueden controlar presentes en un sistema.</span><span class="sxs-lookup"><span data-stu-id="52587-112">You can use the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) function to determine the number of controllable auxiliary devices present in a system.</span></span>

<span data-ttu-id="52587-113">Para obtener información acerca de un dispositivo de audio determinado, use la función [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="52587-113">To get information about a particular auxiliary audio device, use the [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) function.</span></span> <span data-ttu-id="52587-114">Esta función rellena una estructura [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) con información sobre las capacidades de un dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="52587-114">This function fills an [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="52587-115">Esta información incluye los identificadores de fabricante y de producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52587-115">This information includes the manufacturer and product identifiers, a product name for the device, and the device-driver version number.</span></span>

 

 