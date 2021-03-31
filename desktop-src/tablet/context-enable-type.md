---
description: Indica si los mensajes de contexto se deben enviar al procedimiento de ventana de la ventana propietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumeración CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816830"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="61765-103">\_Enumeración de tipo de habilitación de contexto \_</span><span class="sxs-lookup"><span data-stu-id="61765-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="61765-104">Indica si los mensajes de contexto se deben enviar al procedimiento de ventana de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="61765-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="61765-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61765-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="61765-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="61765-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61765-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_Habilitar contexto**</span><span class="sxs-lookup"><span data-stu-id="61765-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="61765-108">El contexto de la tableta debe estar habilitado, lo que da lugar a que se envíen mensajes de contexto al procedimiento de ventana de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="61765-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="61765-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**deshabilitar contexto \_**</span><span class="sxs-lookup"><span data-stu-id="61765-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="61765-110">El contexto de la tableta debe estar deshabilitado, lo que impide que se envíen más mensajes de contexto al procedimiento de ventana o al receptor de eventos de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="61765-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61765-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61765-111">Requirements</span></span>



| <span data-ttu-id="61765-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="61765-112">Requirement</span></span> | <span data-ttu-id="61765-113">Value</span><span class="sxs-lookup"><span data-stu-id="61765-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="61765-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61765-114">Minimum supported client</span></span><br/> | <span data-ttu-id="61765-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="61765-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61765-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61765-116">Minimum supported server</span></span><br/> | <span data-ttu-id="61765-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="61765-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="61765-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="61765-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61765-119">**ITablet:: CreateContext (método)**</span><span class="sxs-lookup"><span data-stu-id="61765-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




