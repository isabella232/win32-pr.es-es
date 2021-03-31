---
title: EnableDCOM
description: Controla la activación global y las directivas de llamada de la máquina. Solo los administradores y el sistema tienen acceso total a esta parte del registro. El resto de usuarios tienen acceso de solo lectura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valor del registro EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418546"
---
# <a name="enabledcom"></a><span data-ttu-id="70640-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="70640-106">EnableDCOM</span></span>

<span data-ttu-id="70640-107">Controla la activación global y las directivas de llamada de la máquina.</span><span class="sxs-lookup"><span data-stu-id="70640-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="70640-108">Solo los administradores y el sistema tienen acceso total a esta parte del registro.</span><span class="sxs-lookup"><span data-stu-id="70640-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="70640-109">El resto de usuarios tienen acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="70640-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="70640-110">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="70640-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="70640-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70640-111">Remarks</span></span>

<span data-ttu-id="70640-112">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="70640-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="70640-113">Value</span><span class="sxs-lookup"><span data-stu-id="70640-113">Value</span></span>    | <span data-ttu-id="70640-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="70640-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70640-115">N (o n)</span><span class="sxs-lookup"><span data-stu-id="70640-115">N (or n)</span></span> | <span data-ttu-id="70640-116">Ningún cliente remoto puede iniciar servidores o conectarse a objetos de este equipo.</span><span class="sxs-lookup"><span data-stu-id="70640-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="70640-117">Los clientes locales no pueden tener acceso a servidores DCOM remotos. se bloquea todo el tráfico DCOM.</span><span class="sxs-lookup"><span data-stu-id="70640-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="70640-118">El inicio local del código de clase y la conexión a objetos se permiten por clase según el valor y los permisos de acceso del valor del registro [**LaunchPermission**](launchpermission.md) de la clase y el valor del registro [**DefaultLaunchPermission**](defaultlaunchpermission.md) global.</span><span class="sxs-lookup"><span data-stu-id="70640-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="70640-119">Y (o y)</span><span class="sxs-lookup"><span data-stu-id="70640-119">Y (or y)</span></span> | <span data-ttu-id="70640-120">El inicio de servidores y la conexión a objetos por parte de clientes remotos se permite por clase según el valor y los permisos de acceso del valor del registro [**LaunchPermission**](launchpermission.md) de la clase y el valor del registro [**DefaultLaunchPermission**](defaultlaunchpermission.md) global.</span><span class="sxs-lookup"><span data-stu-id="70640-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="70640-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70640-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70640-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="70640-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="70640-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="70640-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="70640-124">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="70640-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




