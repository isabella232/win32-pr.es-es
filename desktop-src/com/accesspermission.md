---
title: AccessPermission
description: Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valor del registro AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488314"
---
# <a name="accesspermission"></a><span data-ttu-id="0f824-105">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="0f824-105">AccessPermission</span></span>

<span data-ttu-id="0f824-106">Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0f824-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="0f824-107">Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="0f824-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0f824-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0f824-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="0f824-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f824-109">Remarks</span></span>

<span data-ttu-id="0f824-110">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="0f824-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="0f824-111">Contiene datos que describen la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0f824-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="0f824-112">Al recibir una solicitud para conectarse a un objeto existente de esta clase, se comprueba la ACL de la aplicación a la que se llama durante la suplantación del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="0f824-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="0f824-113">Si se produce un error en la comprobación de acceso, no se permite la conexión.</span><span class="sxs-lookup"><span data-stu-id="0f824-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="0f824-114">Si este valor con nombre no existe, la ACL [**DefaultAccessPermission**](defaultaccesspermission.md) se prueba para determinar si la conexión se va a permitir.</span><span class="sxs-lookup"><span data-stu-id="0f824-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="0f824-115">En el caso de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o no usan la interfaz [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar el AppID, el archivo ejecutable del archivo binario de la aplicación debe estar asignado al AppID de la aplicación, tal y como se describe en [**AppID**](appid.md).</span><span class="sxs-lookup"><span data-stu-id="0f824-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="0f824-116">Esto es necesario para que COM pueda localizar el AppID de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0f824-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f824-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f824-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f824-118">**Fall**</span><span class="sxs-lookup"><span data-stu-id="0f824-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="0f824-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="0f824-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="0f824-120">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="0f824-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 