---
description: En Windows Vista, los contadores de rendimiento implementaron una nueva arquitectura (versión 2,0) para proporcionar los datos del contador.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Proporcionar datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667254"
---
# <a name="providing-counter-data"></a><span data-ttu-id="71169-103">Proporcionar datos de contador</span><span class="sxs-lookup"><span data-stu-id="71169-103">Providing Counter Data</span></span>

<span data-ttu-id="71169-104">Los componentes de software que publican datos mediante los contadores de rendimiento de Windows se denominan proveedores de datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71169-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="71169-105">Windows admite dos tipos de proveedores de datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71169-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="71169-106">Los proveedores de datos de rendimiento heredados (**proveedores v1**) se implementan mediante. Archivo INI y un archivo DLL de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71169-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="71169-107">Los proveedores de datos de rendimiento modernos (**proveedores V2**) usan un. MAN (manifiesto XML) y las API del proveedor de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71169-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="71169-108">Manifiestos</span><span class="sxs-lookup"><span data-stu-id="71169-108">Manifests</span></span>

<span data-ttu-id="71169-109">Los proveedores de datos de rendimiento modernos usan un. MAN (manifiesto XML) para definir los datos del contador y usar las API del proveedor de contadores de rendimiento para administrar los datos en el contexto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="71169-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="71169-110">Los proveedores implementados mediante un manifiesto y las API de proveedor de contadores de rendimiento a menudo se denominan **proveedores V2**.</span><span class="sxs-lookup"><span data-stu-id="71169-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="71169-111">Windows admite proveedores de modo usuario V2 en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="71169-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="71169-112">Para obtener detalles sobre el modo de usuario, consulte [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="71169-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="71169-113">Windows admite proveedores de modo kernel v2 en Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="71169-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="71169-114">Para obtener detalles sobre el modo kernel, consulte [supervisión del rendimiento del modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="71169-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="71169-115">DLL de rendimiento (desusado)</span><span class="sxs-lookup"><span data-stu-id="71169-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="71169-116">En la arquitectura del contador de rendimiento heredado, los proveedores implementaron un archivo DLL de rendimiento en que se ejecutaba en el proceso del consumidor para recopilar y proporcionar los datos del contador cuando un consumidor lo solicitó.</span><span class="sxs-lookup"><span data-stu-id="71169-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="71169-117">El proveedor usó una inicialización (. INI) y entradas del registro para definir los contadores y configurar el archivo DLL de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71169-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="71169-118">Proveedores implementados mediante. El archivo INI y un archivo DLL de rendimiento a menudo se denominan **proveedores v1**.</span><span class="sxs-lookup"><span data-stu-id="71169-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="71169-119">Aunque todavía puede usar un archivo DLL de rendimiento para proporcionar datos de contador, esta arquitectura está en desuso debido a las limitaciones de rendimiento y confiabilidad significativas.</span><span class="sxs-lookup"><span data-stu-id="71169-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="71169-120">Además, los proveedores v1 suelen ser más difíciles de implementar, ya que requieren el envío de un archivo DLL independiente que deba ejecutarse en el proceso del consumidor.</span><span class="sxs-lookup"><span data-stu-id="71169-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="71169-121">Para obtener más información, vea [proporcionar datos de contador mediante un archivo dll de rendimiento](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="71169-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
