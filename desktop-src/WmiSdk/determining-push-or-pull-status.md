---
description: Puede modelar un proveedor de clases como un proveedor de inserción o de extracción, que especifica cómo un proveedor espera interactuar con WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinar el estado de inserción o de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715829"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="7b7d7-103">Determinar el estado de inserción o de extracción</span><span class="sxs-lookup"><span data-stu-id="7b7d7-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="7b7d7-104">Puede modelar un proveedor de clases como un proveedor de inserción o de extracción, que especifica cómo un proveedor espera interactuar con WMI.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="7b7d7-105">Los proveedores de extracción reciben una solicitud de WMI y satisfacen la solicitud mediante la generación dinámica de los datos o la recuperación de una caché local.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="7b7d7-106">Los proveedores de extracción también deben implementar un gran número de interfaces.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="7b7d7-107">Un proveedor de extracción genera dinámicamente definiciones de clase.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="7b7d7-108">Normalmente, los datos administrados por un proveedor de extracción cambian con frecuencia, lo que requiere que el proveedor genere la clase dinámicamente o recupere la clase de una caché local siempre que una aplicación emita una solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="7b7d7-109">Un proveedor de extracción debe implementar sus propios mecanismos de recuperación de datos, caché y notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="7b7d7-110">Dado que la mayoría de los proveedores son proveedores de extracción, la documentación de este archivo supone que está creando un proveedor de extracción, a menos que se indique explícitamente lo contrario.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="7b7d7-111">Por el contrario, WMI usa datos en el repositorio WMI para controlar todas las solicitudes de aplicación para los proveedores de inserciones.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="7b7d7-112">Los proveedores de inserciones también usan menos métodos de interfaz y, por tanto, son más fáciles de implementar.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="7b7d7-113">Un proveedor de inserciones usa el repositorio WMI como área de almacenamiento para obtener información sobre el objeto administrado y actualiza esa información solo durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="7b7d7-114">Por ejemplo, el proveedor de clases WDM incluido en la sección WMI del kit de desarrollo de software (SDK) de Microsoft Windows se modela como un proveedor de inserciones.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="7b7d7-115">Mediante el uso del repositorio WMI como área de almacenamiento, un proveedor de inserción obtiene las siguientes ventajas a través de un proveedor de extracción:</span><span class="sxs-lookup"><span data-stu-id="7b7d7-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="7b7d7-116">No es necesario que el proveedor implemente una memoria caché local para almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="7b7d7-117">No es necesario que el proveedor admita la recuperación de datos. en su lugar, el proveedor puede basarse en WMI para proporcionar compatibilidad de recuperación.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="7b7d7-118">Cuando una aplicación solicita datos proporcionados por el proveedor, WMI cumple esa solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="7b7d7-119">El proveedor también puede basarse en WMI para admitir la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="7b7d7-120">Sin embargo, dado que un proveedor de inserciones solo se actualiza durante la inicialización, es posible que los cambios en una clase no se reflejen en el repositorio WMI durante algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="7b7d7-121">Por lo tanto, el modelo de proveedor de inserciones funciona mejor con las clases que cambian poco o más son completamente estáticas.</span><span class="sxs-lookup"><span data-stu-id="7b7d7-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



