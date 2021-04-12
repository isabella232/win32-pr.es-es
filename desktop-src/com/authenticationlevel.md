---
title: AuthenticationLevel
description: Establece el nivel de autenticación para las aplicaciones que no llaman a CoInitializeSecurity o para las aplicaciones que llaman a CoInitializeSecurity y especifican un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valor del registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357762"
---
# <a name="authenticationlevel"></a><span data-ttu-id="9e8e9-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="9e8e9-104">AuthenticationLevel</span></span>

<span data-ttu-id="9e8e9-105">Establece el nivel de autenticación para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o para las aplicaciones que llaman a **CoInitializeSecurity** y especifican un AppID.</span><span class="sxs-lookup"><span data-stu-id="9e8e9-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9e8e9-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="9e8e9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="9e8e9-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e8e9-107">Remarks</span></span>

<span data-ttu-id="9e8e9-108">Se trata de un valor de **Registro \_ DWORD** equivalente a las constantes de nivel de autenticación de RPC \_ C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9e8e9-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="9e8e9-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8e9-109">Value</span></span> | <span data-ttu-id="9e8e9-110">Constante</span><span class="sxs-lookup"><span data-stu-id="9e8e9-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="9e8e9-111">1</span><span class="sxs-lookup"><span data-stu-id="9e8e9-111">1</span></span>     | <span data-ttu-id="9e8e9-112">nivel de autenticación de RPC \_ C \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="9e8e9-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="9e8e9-113">2</span><span class="sxs-lookup"><span data-stu-id="9e8e9-113">2</span></span>     | <span data-ttu-id="9e8e9-114">\_conexión de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="9e8e9-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="9e8e9-115">3</span><span class="sxs-lookup"><span data-stu-id="9e8e9-115">3</span></span>     | <span data-ttu-id="9e8e9-116">\_llamada de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="9e8e9-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="9e8e9-117">4</span><span class="sxs-lookup"><span data-stu-id="9e8e9-117">4</span></span>     | <span data-ttu-id="9e8e9-118">\_PKT de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="9e8e9-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="9e8e9-119">5</span><span class="sxs-lookup"><span data-stu-id="9e8e9-119">5</span></span>     | <span data-ttu-id="9e8e9-120">integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9e8e9-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="9e8e9-121">6</span><span class="sxs-lookup"><span data-stu-id="9e8e9-121">6</span></span>     | <span data-ttu-id="9e8e9-122">\_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_</span><span class="sxs-lookup"><span data-stu-id="9e8e9-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="9e8e9-123">El valor **AuthenticationLevel** es similar al valor [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8e9-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="9e8e9-124">Si el valor **AuthenticationLevel** está presente, se usa en lugar del valor **LegacyAuthenticationLevel** para ese AppID.</span><span class="sxs-lookup"><span data-stu-id="9e8e9-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="9e8e9-125">Si el valor de **AuthenticationLevel** es del tipo incorrecto o está fuera del intervalo, se produce un error en [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , lo que provoca un error en la serialización de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9e8e9-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="9e8e9-126">Esto evita que la aplicación realice llamadas en todo (entre apartamentos, entre subprocesos, entre procesos o entre equipos).</span><span class="sxs-lookup"><span data-stu-id="9e8e9-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="9e8e9-127">Los valores **AuthenticationLevel** y [**AccessPermission**](accesspermission.md) son independientes.</span><span class="sxs-lookup"><span data-stu-id="9e8e9-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="9e8e9-128">Si no hay ninguno, se usa el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9e8e9-128">If one is not present, the default is used.</span></span> <span data-ttu-id="9e8e9-129">Las siguientes reglas muestran la interacción entre el valor de **AuthenticationLevel** y el valor de **AccessPermission** :</span><span class="sxs-lookup"><span data-stu-id="9e8e9-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="9e8e9-130">Si **AuthenticationLevel** es None, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).</span><span class="sxs-lookup"><span data-stu-id="9e8e9-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="9e8e9-131">Si **AuthenticationLevel** no está presente y [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) es None, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).</span><span class="sxs-lookup"><span data-stu-id="9e8e9-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e8e9-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e8e9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e8e9-133">Constantes de nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="9e8e9-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="9e8e9-134">**LegacyAuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="9e8e9-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="9e8e9-135">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="9e8e9-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="9e8e9-136">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="9e8e9-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




