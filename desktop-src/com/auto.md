---
title: Automático
description: Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC de COM.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704803"
---
# <a name="auto"></a><span data-ttu-id="2ec0d-103">Automático</span><span class="sxs-lookup"><span data-stu-id="2ec0d-103">Auto</span></span>

<span data-ttu-id="2ec0d-104">Determina si el depurador se inicia automáticamente cuando se envía una notificación RPC de COM.</span><span class="sxs-lookup"><span data-stu-id="2ec0d-104">Determines if the debugger is automatically launched when a COM RPC notification is sent.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2ec0d-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="2ec0d-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a><span data-ttu-id="2ec0d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ec0d-106">Remarks</span></span>

<span data-ttu-id="2ec0d-107">Se trata de un valor de **\_ palabra de registro** .</span><span class="sxs-lookup"><span data-stu-id="2ec0d-107">This is a **REG\_WORD** value.</span></span>



| <span data-ttu-id="2ec0d-108">Value</span><span class="sxs-lookup"><span data-stu-id="2ec0d-108">Value</span></span> | <span data-ttu-id="2ec0d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ec0d-109">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="2ec0d-110">1</span><span class="sxs-lookup"><span data-stu-id="2ec0d-110">1</span></span>     | <span data-ttu-id="2ec0d-111">Iniciar el depurador automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2ec0d-111">Automatically launch debugger.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2ec0d-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ec0d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ec0d-113">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="2ec0d-113">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="2ec0d-114">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="2ec0d-114">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> <dt>

[<span data-ttu-id="2ec0d-115">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="2ec0d-115">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> </dl>

 

 




