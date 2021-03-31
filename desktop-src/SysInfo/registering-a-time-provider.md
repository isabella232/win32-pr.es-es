---
description: El sistema carga un proveedor de hora en función de su información de configuración almacenada en el registro.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrar un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910325"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="f6431-103">Registrar un proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="f6431-103">Registering a Time Provider</span></span>

<span data-ttu-id="f6431-104">El sistema carga un proveedor de hora en función de su información de configuración almacenada en el registro.</span><span class="sxs-lookup"><span data-stu-id="f6431-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="f6431-105">Cada proveedor de hora debe crear la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="f6431-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="f6431-106">**HKEY \_ \_Equipo local \\ sistema** \\ **CurrentControlSet** \\ **servicios** \\ **W32Time** \\ **TimeProviders** \\ *providerName*</span><span class="sxs-lookup"><span data-stu-id="f6431-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="f6431-107">En la tabla siguiente se describen los valores que deben existir en la clave de cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="f6431-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="f6431-108">Value</span><span class="sxs-lookup"><span data-stu-id="f6431-108">Value</span></span>             | <span data-ttu-id="f6431-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6431-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6431-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="f6431-110">**DllName**</span></span>       | <span data-ttu-id="f6431-111">Nombre del archivo DLL que contiene el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f6431-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="f6431-112">Este valor tiene el tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="f6431-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="f6431-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="f6431-113">**Enabled**</span></span>       | <span data-ttu-id="f6431-114">Indica si se debe iniciar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f6431-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="f6431-115">Si este valor es 1, se inicia el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f6431-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="f6431-116">De lo contrario, el proveedor no se inicia.</span><span class="sxs-lookup"><span data-stu-id="f6431-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="f6431-117">Este valor tiene el tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f6431-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="f6431-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="f6431-118">**InputProvider**</span></span> | <span data-ttu-id="f6431-119">Indica si el proveedor es un proveedor de entrada o un proveedor de salida.</span><span class="sxs-lookup"><span data-stu-id="f6431-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="f6431-120">Si este valor es 1, el proveedor es un proveedor de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6431-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="f6431-121">De lo contrario, el proveedor es un proveedor de salida.</span><span class="sxs-lookup"><span data-stu-id="f6431-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="f6431-122">Este valor tiene el tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f6431-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="f6431-123">El administrador de proveedores de hora enumera las claves en la clave **TimeProviders** e inicia cada proveedor habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6431-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="f6431-124">Los proveedores se inician en el inicio del sistema y cada vez que hay cambios en los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f6431-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="f6431-125">Cada proveedor de hora también puede almacenar información de configuración específica de la aplicación en el registro.</span><span class="sxs-lookup"><span data-stu-id="f6431-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



