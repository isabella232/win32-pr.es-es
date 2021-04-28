---
description: Nuevos Low-Level binarios
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuevos Low-Level binarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088073"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="e2c74-103">Nuevos Low-Level binarios</span><span class="sxs-lookup"><span data-stu-id="e2c74-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e2c74-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="e2c74-104">Affected Platforms</span></span>

<span data-ttu-id="e2c74-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2c74-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e2c74-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2c74-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e2c74-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="e2c74-107">Feature Impact</span></span>

<span data-ttu-id="e2c74-108">**Gravedad:** media</span><span class="sxs-lookup"><span data-stu-id="e2c74-108">**Severity** - Medium</span></span>  
<span data-ttu-id="e2c74-109">**Frecuencia:** alta</span><span class="sxs-lookup"><span data-stu-id="e2c74-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="e2c74-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2c74-110">Description</span></span>

<span data-ttu-id="e2c74-111">Para mejorar las eficiencias de ingeniería internas y mejorar las bases para el trabajo futuro, hemos reubicado algunas funcionalidades en nuevos archivos binarios de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="e2c74-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="e2c74-112">Esta refactorización permitirá que futuras instalaciones de Windows proporcionen subconjuntos de funcionalidad para reducir el área de superficie (requisitos de disco y memoria, mantenimiento y superficie de ataque).</span><span class="sxs-lookup"><span data-stu-id="e2c74-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e2c74-113">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="e2c74-113">Manifestation of Impact</span></span>

<span data-ttu-id="e2c74-114">Como ejemplo de funcionalidad que hemos movido a archivos binarios de bajo nivel, kernelbase.dll la funcionalidad de kernel32.dll y advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e2c74-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="e2c74-115">Esto significa que el binario existente ahora reenvía las llamadas al nuevo binario en lugar de controlarlas directamente; el reenvío puede ser estático (la tabla de exportación muestra el redireccionamiento) o en tiempo de ejecución (el archivo DLL tiene una rutina de código auxiliar que llama al nuevo binario).</span><span class="sxs-lookup"><span data-stu-id="e2c74-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="e2c74-116">Esto afectará a las aplicaciones de bajo nivel, como las aplicaciones de seguridad y de copia de seguridad que dependen de las API internas y los desplazamientos.</span><span class="sxs-lookup"><span data-stu-id="e2c74-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="e2c74-117">Solución</span><span class="sxs-lookup"><span data-stu-id="e2c74-117">Solution</span></span>

<span data-ttu-id="e2c74-118">El único impacto es el código que realiza suposiciones al intentar ver la tabla de exportación kernel32.dll o advapi32.dll en memoria, como una aplicación antivirus.</span><span class="sxs-lookup"><span data-stu-id="e2c74-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="e2c74-119">Use las API publicadas y no los detalles de su implementación.</span><span class="sxs-lookup"><span data-stu-id="e2c74-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="e2c74-120">Este es solo un ejemplo de implementación en torno a un detalle de implementación para una API.</span><span class="sxs-lookup"><span data-stu-id="e2c74-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



