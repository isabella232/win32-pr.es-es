---
title: ActivationFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error de inicio y activación de componentes.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valor del registro ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419145"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="11925-104">ActivationFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="11925-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="11925-105">Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error de inicio y activación de componentes.</span><span class="sxs-lookup"><span data-stu-id="11925-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="11925-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="11925-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="11925-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11925-107">Remarks</span></span>

<span data-ttu-id="11925-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="11925-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="11925-109">Value</span><span class="sxs-lookup"><span data-stu-id="11925-109">Value</span></span> | <span data-ttu-id="11925-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="11925-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11925-111">0</span><span class="sxs-lookup"><span data-stu-id="11925-111">0</span></span>     | <span data-ttu-id="11925-112">Use el registro discrecional.</span><span class="sxs-lookup"><span data-stu-id="11925-112">Use discretionary logging.</span></span> <span data-ttu-id="11925-113">Registrar errores de forma predeterminada, pero los clientes pueden invalidar este comportamiento mediante la especificación \_ de CLSCTX ningún \_ \_ registro de errores en [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span><span class="sxs-lookup"><span data-stu-id="11925-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="11925-114">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="11925-114">This is the default value.</span></span> |
| <span data-ttu-id="11925-115">1</span><span class="sxs-lookup"><span data-stu-id="11925-115">1</span></span>     | <span data-ttu-id="11925-116">Registre siempre todos los errores independientemente del cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="11925-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="11925-117">2</span><span class="sxs-lookup"><span data-stu-id="11925-117">2</span></span>     | <span data-ttu-id="11925-118">Nunca registre ningún error independientemente de lo que haya especificado el cliente.</span><span class="sxs-lookup"><span data-stu-id="11925-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="11925-119">Si necesita una aplicación para controlar el registro de eventos, se recomienda establecer este valor en 0 y escribir el código de cliente para invalidarlo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11925-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="11925-120">Se recomienda encarecidamente no establecer el valor en 2.</span><span class="sxs-lookup"><span data-stu-id="11925-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="11925-121">Si el registro de eventos está deshabilitado, es más difícil diagnosticar los problemas.</span><span class="sxs-lookup"><span data-stu-id="11925-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="11925-122">En el caso de los errores de permisos de restricciones del equipo, en los que COM no tiene los bits CLSCTX, COM tratará un valor de 0 como 1.</span><span class="sxs-lookup"><span data-stu-id="11925-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11925-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11925-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11925-124">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="11925-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




