---
title: LegacyImpersonationLevel
description: Establece el nivel de suplantación predeterminado para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valor del registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704679"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="d8cb4-104">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="d8cb4-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="d8cb4-105">Establece el nivel de suplantación predeterminado para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d8cb4-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="d8cb4-106">No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="d8cb4-107">Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="d8cb4-108">Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="d8cb4-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="d8cb4-109">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="d8cb4-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="d8cb4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8cb4-110">Remarks</span></span>

<span data-ttu-id="d8cb4-111">Se trata de un valor de **\_ palabra de registro** equivalente a las \_ \_ constantes de nivel Imp de RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="d8cb4-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="d8cb4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d8cb4-112">Value</span></span> | <span data-ttu-id="d8cb4-113">Constante</span><span class="sxs-lookup"><span data-stu-id="d8cb4-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="d8cb4-114">1</span><span class="sxs-lookup"><span data-stu-id="d8cb4-114">1</span></span>     | <span data-ttu-id="d8cb4-115">\_nivel Imp de RPC C \_ \_ \_ anónimo</span><span class="sxs-lookup"><span data-stu-id="d8cb4-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="d8cb4-116">2</span><span class="sxs-lookup"><span data-stu-id="d8cb4-116">2</span></span>     | <span data-ttu-id="d8cb4-117">\_identidad de \_ \_ nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="d8cb4-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="d8cb4-118">3</span><span class="sxs-lookup"><span data-stu-id="d8cb4-118">3</span></span>     | <span data-ttu-id="d8cb4-119">\_ \_ \_ Impersonate de nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="d8cb4-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="d8cb4-120">4</span><span class="sxs-lookup"><span data-stu-id="d8cb4-120">4</span></span>     | <span data-ttu-id="d8cb4-121">\_delegado de \_ \_ nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="d8cb4-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="d8cb4-122">Si este valor del registro no está presente, el nivel de suplantación predeterminado establecido por el sistema es 2 (se identifica el nivel de Imp de RPC \_ C \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="d8cb4-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8cb4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8cb4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8cb4-124">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="d8cb4-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="d8cb4-125">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="d8cb4-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




