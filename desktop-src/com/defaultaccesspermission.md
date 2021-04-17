---
title: DefaultAccessPermission
description: Establece la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las clases para las que no hay ningún valor AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valor del registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704571"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="ab533-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="ab533-104">DefaultAccessPermission</span></span>

<span data-ttu-id="ab533-105">Establece la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las clases para las que no hay ningún valor [**AccessPermission**](accesspermission.md) .</span><span class="sxs-lookup"><span data-stu-id="ab533-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="ab533-106">Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y no tienen un valor **AccessPermission** bajo su clave [**AppID**](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="ab533-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="ab533-107">No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab533-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="ab533-108">Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="ab533-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="ab533-109">Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="ab533-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="ab533-110">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="ab533-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="ab533-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab533-111">Remarks</span></span>

<span data-ttu-id="ab533-112">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="ab533-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="ab533-113">El tiempo de ejecución de COM en el servidor comprueba la ACL descrita por este valor durante la suplantación del autor de la llamada que está intentando conectarse al objeto y su éxito determina si se permite o no el acceso.</span><span class="sxs-lookup"><span data-stu-id="ab533-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="ab533-114">Si se produce un error en la comprobación de acceso, no se permite la conexión con el objeto.</span><span class="sxs-lookup"><span data-stu-id="ab533-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="ab533-115">Si este valor con nombre no existe, solo se permite a la entidad de seguridad del servidor y al sistema local llamar al servidor.</span><span class="sxs-lookup"><span data-stu-id="ab533-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="ab533-116">De forma predeterminada, este valor no tiene ninguna entrada.</span><span class="sxs-lookup"><span data-stu-id="ab533-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="ab533-117">Solo la entidad de seguridad de servidor y el sistema pueden llamar al servidor.</span><span class="sxs-lookup"><span data-stu-id="ab533-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="ab533-118">Este valor proporciona un nivel simple de administración centralizada del acceso de conexión predeterminado a los objetos en ejecución en un equipo.</span><span class="sxs-lookup"><span data-stu-id="ab533-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab533-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab533-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab533-120">**AccessPermission**</span><span class="sxs-lookup"><span data-stu-id="ab533-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="ab533-121">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="ab533-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="ab533-122">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="ab533-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




