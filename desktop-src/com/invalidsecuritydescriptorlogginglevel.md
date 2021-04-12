---
title: InvalidSecurityDescriptorLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos acerca de los descriptores de seguridad no válidos para el inicio y los permisos de acceso de los componentes.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valor del registro InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356673"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="d3d66-104">InvalidSecurityDescriptorLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="d3d66-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="d3d66-105">Establece el nivel de detalle de las entradas del registro de eventos acerca de los descriptores de seguridad no válidos para el inicio y los permisos de acceso de los componentes.</span><span class="sxs-lookup"><span data-stu-id="d3d66-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d3d66-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="d3d66-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="d3d66-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3d66-107">Remarks</span></span>

<span data-ttu-id="d3d66-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d3d66-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d3d66-109">Value</span><span class="sxs-lookup"><span data-stu-id="d3d66-109">Value</span></span> | <span data-ttu-id="d3d66-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3d66-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d66-111">1</span><span class="sxs-lookup"><span data-stu-id="d3d66-111">1</span></span>     | <span data-ttu-id="d3d66-112">Registre siempre los errores cuando COM encuentre un descriptor de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="d3d66-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="d3d66-113">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d3d66-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="d3d66-114">2</span><span class="sxs-lookup"><span data-stu-id="d3d66-114">2</span></span>     | <span data-ttu-id="d3d66-115">Nunca Registre errores cuando COM encuentre un descriptor de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="d3d66-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="d3d66-116">No se recomienda deshabilitar el registro de eventos, ya que puede dificultar el diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="d3d66-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="d3d66-117">Si establece los descriptores de seguridad de permisos de inicio y acceso (normalmente denominados ACL) directamente, es posible crear un descriptor de seguridad cuyo significado no se pueda interpretar de forma no ambigua.</span><span class="sxs-lookup"><span data-stu-id="d3d66-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="d3d66-118">COM realiza una entrada en el registro de eventos cuando encuentra un descriptor de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="d3d66-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="d3d66-119">Tenga en cuenta que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) y [**CallFailureLoggingLevel**](callfailurelogginglevel.md) no tienen ningún control sobre el registro de errores de descriptor de seguridad no válidos.</span><span class="sxs-lookup"><span data-stu-id="d3d66-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="d3d66-120">Use **InvalidSecurityDescriptorLoggingLevel** para tener un control total sobre esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="d3d66-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3d66-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3d66-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3d66-122">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="d3d66-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




