---
title: LaunchPermission
description: Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase. Este valor se puede Agregar bajo cualquier clave AppID para limitar la activación por parte de clientes remotos de clases concretas.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valor del registro LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076373"
---
# <a name="launchpermission"></a><span data-ttu-id="a8de8-105">LaunchPermission</span><span class="sxs-lookup"><span data-stu-id="a8de8-105">LaunchPermission</span></span>

<span data-ttu-id="a8de8-106">Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase.</span><span class="sxs-lookup"><span data-stu-id="a8de8-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="a8de8-107">Este valor se puede Agregar bajo cualquier clave [**AppID**](appid-key.md) para limitar la activación por parte de clientes remotos de clases concretas.</span><span class="sxs-lookup"><span data-stu-id="a8de8-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a8de8-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="a8de8-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="a8de8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8de8-109">Remarks</span></span>

<span data-ttu-id="a8de8-110">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="a8de8-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="a8de8-111">Al recibir una solicitud local o remota para iniciar el servidor de esta clase, la ACL descrita por este valor se comprueba durante la suplantación del cliente y su éxito permite o impide el inicio del servidor.</span><span class="sxs-lookup"><span data-stu-id="a8de8-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="a8de8-112">Si este valor no existe, el valor de [**DefaultLaunchPermission**](defaultlaunchpermission.md) se comprueba de la misma manera para determinar si se puede iniciar el código de clase.</span><span class="sxs-lookup"><span data-stu-id="a8de8-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8de8-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8de8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8de8-114">**Fall**</span><span class="sxs-lookup"><span data-stu-id="a8de8-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="a8de8-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="a8de8-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="a8de8-116">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="a8de8-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




