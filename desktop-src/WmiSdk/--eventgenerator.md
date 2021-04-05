---
description: Actúa como clase primaria para las clases que controlan la generación de eventos, como los eventos de temporizador.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279463"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="b15ba-103">\_\_Clase EventGenerator</span><span class="sxs-lookup"><span data-stu-id="b15ba-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="b15ba-104">La clase del sistema **\_ \_ EventGenerator** es una clase base abstracta que actúa como clase primaria para las clases que controlan la generación de eventos, como [los eventos de temporizador](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="b15ba-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="b15ba-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b15ba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b15ba-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b15ba-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15ba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b15ba-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="b15ba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b15ba-108">Members</span></span>

<span data-ttu-id="b15ba-109">La clase **\_ \_ EventGenerator** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="b15ba-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15ba-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b15ba-110">Remarks</span></span>

<span data-ttu-id="b15ba-111">La clase **\_ \_ EventGenerator** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="b15ba-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15ba-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b15ba-112">Requirements</span></span>



| <span data-ttu-id="b15ba-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b15ba-113">Requirement</span></span> | <span data-ttu-id="b15ba-114">Value</span><span class="sxs-lookup"><span data-stu-id="b15ba-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b15ba-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15ba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b15ba-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b15ba-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b15ba-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15ba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b15ba-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b15ba-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b15ba-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b15ba-119">Namespace</span></span><br/>                | <span data-ttu-id="b15ba-120">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="b15ba-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b15ba-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b15ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15ba-122">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="b15ba-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="b15ba-123">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b15ba-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

