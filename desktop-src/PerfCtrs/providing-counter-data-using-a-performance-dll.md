---
description: Un servicio, un controlador o una aplicación que desee proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Proporcionar datos de contadores mediante un archivo DLL de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667259"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="15d9b-103">Proporcionar datos de contadores mediante un archivo DLL de rendimiento</span><span class="sxs-lookup"><span data-stu-id="15d9b-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15d9b-104">Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="15d9b-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="15d9b-105">En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método también.</span><span class="sxs-lookup"><span data-stu-id="15d9b-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="15d9b-106">Un servicio, un controlador o una aplicación que desee proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos.</span><span class="sxs-lookup"><span data-stu-id="15d9b-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="15d9b-107">Cuando un consumidor consulta datos de rendimiento, el sistema carga la DLL del proveedor en el proceso del consumidor y llama al proveedor para recopilar los datos.</span><span class="sxs-lookup"><span data-stu-id="15d9b-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="15d9b-108">Para obtener más información sobre cómo escribir el archivo DLL de rendimiento, consulte [crear un archivo dll de extensión de rendimiento](creating-a-performance-extension-dll.md).</span><span class="sxs-lookup"><span data-stu-id="15d9b-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="15d9b-109">El sistema utiliza el registro para determinar a qué proveedor se debe llamar.</span><span class="sxs-lookup"><span data-stu-id="15d9b-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="15d9b-110">Para obtener información sobre cómo registrar el proveedor y los contadores que admite, vea [Agregar contadores de rendimiento](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="15d9b-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="15d9b-111">Los archivos dll de rendimiento no se admiten en Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="15d9b-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="15d9b-112">Si escribe un componente que se debe ejecutar en Windows OneCore, use el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="15d9b-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
