---
title: LegacySecureReferences
description: Determina si las invocaciones de AddRef/Release están protegidas para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valor del registro LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704680"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="8ec51-104">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="8ec51-104">LegacySecureReferences</span></span>

<span data-ttu-id="8ec51-105">Determina si  / las invocaciones de **liberación** de AddRef están protegidas para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="8ec51-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8ec51-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="8ec51-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="8ec51-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ec51-107">Remarks</span></span>

<span data-ttu-id="8ec51-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="8ec51-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="8ec51-109">Un valor de ' Y ' o ' y ' indica que **AddRef** y **Release** están protegidos.</span><span class="sxs-lookup"><span data-stu-id="8ec51-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="8ec51-110">Si este valor del registro no está presente o está establecido en un valor distinto de ' Y ' o ' y ', **AddRef** y **Release** no se protegen.</span><span class="sxs-lookup"><span data-stu-id="8ec51-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="8ec51-111">Al habilitar las referencias seguras, se ralentizan las llamadas remotas.</span><span class="sxs-lookup"><span data-stu-id="8ec51-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ec51-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ec51-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ec51-113">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="8ec51-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="8ec51-114">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="8ec51-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




