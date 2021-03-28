---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister función)
description: Anula el registro de un evento.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149242"
---
# <a name="etweventunregister-function"></a><span data-ttu-id="924bb-103">EtwEventUnregister función)</span><span class="sxs-lookup"><span data-stu-id="924bb-103">EtwEventUnregister function</span></span>


## <a name="description"></a><span data-ttu-id="924bb-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="924bb-104">Description</span></span>


<span data-ttu-id="924bb-105">El <b>EtwEventUnregister</b> anula el registro de un evento.</span><span class="sxs-lookup"><span data-stu-id="924bb-105">The <b>EtwEventUnregister</b> unregisters an event.</span></span>
            

<span data-ttu-id="924bb-106">Los proveedores solo pueden llamar a esta función desde su función <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> .</span><span class="sxs-lookup"><span data-stu-id="924bb-106">Providers can only call this function from their <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> function.</span></span>


## <a name="parameters"></a><span data-ttu-id="924bb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="924bb-107">Parameters</span></span>




### <a name="reghandle-in"></a><span data-ttu-id="924bb-108">RegHandle [in]</span><span class="sxs-lookup"><span data-stu-id="924bb-108">RegHandle [in]</span></span>

<span data-ttu-id="924bb-109">Identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="924bb-109">Handle to an event.</span></span>


## <a name="returns"></a><span data-ttu-id="924bb-110">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="924bb-110">Returns</span></span>



<span data-ttu-id="924bb-111">Devuelve un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="924bb-111">Returns an HRESULT.</span></span>





## <a name="remarks"></a><span data-ttu-id="924bb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="924bb-112">Remarks</span></span>



## <a name="see-also"></a><span data-ttu-id="924bb-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="924bb-113">See also</span></span>