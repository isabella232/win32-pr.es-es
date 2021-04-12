---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuevos archivos binarios de Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278218"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="3cacf-103">Nuevos archivos binarios de Low-Level</span><span class="sxs-lookup"><span data-stu-id="3cacf-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="3cacf-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="3cacf-104">Affected Platforms</span></span>

<span data-ttu-id="3cacf-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="3cacf-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="3cacf-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3cacf-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="3cacf-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="3cacf-107">Feature Impact</span></span>

<span data-ttu-id="3cacf-108">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="3cacf-108">**Severity** - Medium</span></span>  
<span data-ttu-id="3cacf-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="3cacf-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="3cacf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cacf-110">Description</span></span>

<span data-ttu-id="3cacf-111">Para mejorar las eficiencias de ingeniería internas y mejorar las bases de trabajo en el futuro, hemos reubicado alguna funcionalidad para los nuevos archivos binarios de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="3cacf-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="3cacf-112">Esta refactorización hará posible que las instalaciones futuras de Windows proporcionen subconjuntos de funcionalidad para reducir el área expuesta (requisitos de disco y memoria, mantenimiento y superficie expuesta a ataques).</span><span class="sxs-lookup"><span data-stu-id="3cacf-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="3cacf-113">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="3cacf-113">Manifestation of Impact</span></span>

<span data-ttu-id="3cacf-114">Como ejemplo de funcionalidad que se ha migrado a archivos binarios de bajo nivel, kernelbase.dll obtiene la funcionalidad de kernel32.dll y advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="3cacf-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="3cacf-115">Esto significa que el binario existente ahora reenvía las llamadas al nuevo binario en lugar de controlarlas directamente; el reenvío puede ser estático (la tabla de exportación muestra el redireccionamiento) o en tiempo de ejecución (el archivo dll tiene una rutina de código auxiliar que llama al nuevo binario).</span><span class="sxs-lookup"><span data-stu-id="3cacf-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="3cacf-116">Esto afectará a las aplicaciones de bajo nivel como la seguridad y las aplicaciones de copia de seguridad que dependen de las API internas y los desplazamientos.</span><span class="sxs-lookup"><span data-stu-id="3cacf-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="3cacf-117">Solución</span><span class="sxs-lookup"><span data-stu-id="3cacf-117">Solution</span></span>

<span data-ttu-id="3cacf-118">El único impacto es el código que realiza suposiciones al intentar examinar el kernel32.dll o la advapi32.dll Exportar tabla en memoria, como puede ser una aplicación antivirus.</span><span class="sxs-lookup"><span data-stu-id="3cacf-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="3cacf-119">Usar API publicadas y no los detalles de su implementación.</span><span class="sxs-lookup"><span data-stu-id="3cacf-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="3cacf-120">Este es solo un ejemplo de la implementación en torno a un detalle de la implementación de una API.</span><span class="sxs-lookup"><span data-stu-id="3cacf-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



