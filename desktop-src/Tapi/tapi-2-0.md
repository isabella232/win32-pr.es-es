---
description: TAPI 2,0 proporciona un pequeño número de mejoras en la funcionalidad básica de TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360684"
---
# <a name="tapi-20"></a><span data-ttu-id="2ed9d-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="2ed9d-103">TAPI 2.0</span></span>

<span data-ttu-id="2ed9d-104">TAPI 2,0 proporciona un pequeño número de mejoras en la funcionalidad básica de TAPI 1,4.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="2ed9d-105">Sin embargo, se han producido algunos cambios importantes en la arquitectura que mejoran considerablemente su estabilidad.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="2ed9d-106">La mayoría de los cambios eran cambios fundamentales necesarios para incorporar TAPI a Windows NT 4,0 y aprovechar sus características (soporte completo de 32 bits, servicios y Unicode).</span><span class="sxs-lookup"><span data-stu-id="2ed9d-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="2ed9d-107">Sin embargo, estos cambios eran internos en TAPI y apenas tenían efecto en las aplicaciones TAPI.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="2ed9d-108">Las aplicaciones que admiten TAPI 1,3 y 1,4 (aplicaciones de 16 bits por medio de una capa de sistema operativo) funcionan bien en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 y Windows NT.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="2ed9d-109">Sin embargo, el efecto en los desarrolladores de proveedores de servicios era significativo.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="2ed9d-110">Los proveedores de servicios de estos sistemas operativos deben ser archivos dll Unicode de 32 bits completamente que se puedan ejecutar en el contexto de TAPISRV, no en el contexto de la aplicación TAPI (como ocurría en todas las profesionales basadas en Win16 anteriores).</span><span class="sxs-lookup"><span data-stu-id="2ed9d-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="2ed9d-111">Profesionales diseñado para TAPI 1,4 no funcionan en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 ni Windows NT.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="2ed9d-112">TAPI 2,0 también agrega las características importantes del soporte técnico del centro de llamadas y la compatibilidad con calidad de servicio (QOS).</span><span class="sxs-lookup"><span data-stu-id="2ed9d-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="2ed9d-113">Los archivos binarios del sistema TAPI que incluye Windows admiten las versiones 1,3 y 1,4 de TAPI para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="2ed9d-114">Sin embargo, las aplicaciones de 16 bits no pueden usar TAPI 2,0 y no se puede usar un TSP TAPI 2. x de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2ed9d-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



