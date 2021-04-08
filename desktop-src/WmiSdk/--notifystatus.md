---
description: Actúa como clase primaria para las clases de error definidas por el proveedor.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817611"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="eb915-103">\_\_Clase NotifyStatus</span><span class="sxs-lookup"><span data-stu-id="eb915-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="eb915-104">La clase de sistema abstracta **\_ \_ NotifyStatus** actúa como clase primaria para las clases de error definidas por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="eb915-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="eb915-105">La siguiente sintaxis se simplifica desde el código Managed Object Format (MF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eb915-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb915-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb915-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="eb915-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb915-107">Members</span></span>

<span data-ttu-id="eb915-108">La clase **\_ \_ NotifyStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb915-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="eb915-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb915-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb915-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb915-110">Properties</span></span>

<span data-ttu-id="eb915-111">La clase **\_ \_ NotifyStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb915-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb915-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="eb915-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb915-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb915-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb915-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb915-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb915-115">Contiene un código de error o de información para una operación.</span><span class="sxs-lookup"><span data-stu-id="eb915-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="eb915-116">Puede ser cualquier código definido por el usuario, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb915-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb915-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb915-117">Remarks</span></span>

<span data-ttu-id="eb915-118">Aunque la clase **\_ \_ NotifyStatus** puede ser la clase primaria para las clases de error definidas por el proveedor, se recomienda que los proveedores deriven clases de error de [**\_ \_ ExtendedStatus**](--extendedstatus.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="eb915-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="eb915-119">El uso de **\_ \_ ExtendedStatus** permite una mayor estandarización de las clases de error.</span><span class="sxs-lookup"><span data-stu-id="eb915-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="eb915-120">Los proveedores nunca deben crear instancias de **\_ \_ NotifyStatus** directamente, ya que estas instancias no transmiten más información que un código de retorno simple.</span><span class="sxs-lookup"><span data-stu-id="eb915-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb915-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb915-121">Requirements</span></span>



| <span data-ttu-id="eb915-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb915-122">Requirement</span></span> | <span data-ttu-id="eb915-123">Value</span><span class="sxs-lookup"><span data-stu-id="eb915-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="eb915-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb915-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb915-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb915-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="eb915-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb915-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb915-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb915-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="eb915-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb915-128">Namespace</span></span><br/>                | <span data-ttu-id="eb915-129">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="eb915-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="eb915-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb915-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb915-131">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="eb915-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




