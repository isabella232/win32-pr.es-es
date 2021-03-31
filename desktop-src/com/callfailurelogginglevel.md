---
title: CallFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valor del registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903345"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="a06b5-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="a06b5-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="a06b5-105">Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.</span><span class="sxs-lookup"><span data-stu-id="a06b5-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a06b5-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="a06b5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="a06b5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a06b5-107">Remarks</span></span>

<span data-ttu-id="a06b5-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a06b5-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="a06b5-109">Value</span><span class="sxs-lookup"><span data-stu-id="a06b5-109">Value</span></span> | <span data-ttu-id="a06b5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a06b5-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a06b5-111">1</span><span class="sxs-lookup"><span data-stu-id="a06b5-111">1</span></span>     | <span data-ttu-id="a06b5-112">Registre siempre los errores durante una llamada en el proceso de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="a06b5-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="a06b5-113">2</span><span class="sxs-lookup"><span data-stu-id="a06b5-113">2</span></span>     | <span data-ttu-id="a06b5-114">Nunca Registre errores durante una llamada en el proceso de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="a06b5-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="a06b5-115">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a06b5-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a06b5-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a06b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a06b5-117">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="a06b5-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




