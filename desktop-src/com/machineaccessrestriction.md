---
title: MachineAccessRestriction
description: Establece la Directiva de restricción para todo el equipo para el acceso a componentes.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valor del registro MachineAccessRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695420"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="c9e19-104">MachineAccessRestriction</span><span class="sxs-lookup"><span data-stu-id="c9e19-104">MachineAccessRestriction</span></span>

<span data-ttu-id="c9e19-105">Establece la Directiva de restricción para todo el equipo para el acceso a componentes.</span><span class="sxs-lookup"><span data-stu-id="c9e19-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="c9e19-106">Cambiar este valor afectará a todas las aplicaciones de servidor COM y puede impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="c9e19-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="c9e19-107">Si hay aplicaciones de servidor COM con restricciones que son menos rigurosas que las restricciones en todo el equipo, reducir las restricciones en todo el equipo puede exponer estas aplicaciones al acceso no deseado.</span><span class="sxs-lookup"><span data-stu-id="c9e19-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="c9e19-108">Por el contrario, si aumenta las restricciones en todo el equipo, es posible que algunas aplicaciones de servidor COM dejen de ser accesibles mediante la llamada a aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c9e19-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="c9e19-109">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="c9e19-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="c9e19-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9e19-110">Remarks</span></span>

<span data-ttu-id="c9e19-111">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="c9e19-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="c9e19-112">Las entidades de seguridad a las que no se conceden permisos aquí no pueden obtenerlas aunque el valor del registro [DefaultAccessPermission](defaultaccesspermission.md) o la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) concedan los permisos.</span><span class="sxs-lookup"><span data-stu-id="c9e19-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="c9e19-113">De forma predeterminada, los miembros del grupo todos pueden obtener permisos de acceso local y remoto, y los usuarios anónimos pueden obtener permisos de acceso local.</span><span class="sxs-lookup"><span data-stu-id="c9e19-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9e19-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9e19-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9e19-115">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="c9e19-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




