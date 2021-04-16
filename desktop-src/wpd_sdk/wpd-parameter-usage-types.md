---
description: El \_ tipo de \_ \_ enumeración de tipos de uso de parámetros de WPD describe cómo se utiliza un parámetro de método en un método determinado.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumeración WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649695"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="55b77-103">\_ \_ Enumeración de tipos de uso de parámetros de WPD \_</span><span class="sxs-lookup"><span data-stu-id="55b77-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="55b77-104">El tipo de enumeración de tipos de uso de parámetros de WPD describe cómo se utiliza un parámetro de método en un método determinado. [**\_ \_ \_**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types)</span><span class="sxs-lookup"><span data-stu-id="55b77-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b77-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55b77-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="55b77-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="55b77-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="55b77-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_devolución del \_ uso del parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55b77-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="55b77-108">El parámetro recibe el valor devuelto, si lo especifica el método.</span><span class="sxs-lookup"><span data-stu-id="55b77-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="55b77-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ uso de parámetros \_ de WPD en**</span><span class="sxs-lookup"><span data-stu-id="55b77-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="55b77-110">El parámetro contiene un valor de entrada antes de que se llame al método.</span><span class="sxs-lookup"><span data-stu-id="55b77-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="55b77-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**uso de parámetros de WPD \_ \_ \_ fuera**</span><span class="sxs-lookup"><span data-stu-id="55b77-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="55b77-112">El parámetro contiene un valor de salida cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="55b77-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="55b77-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**uso de parámetros de WPD \_ \_ \_ INOUT**</span><span class="sxs-lookup"><span data-stu-id="55b77-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="55b77-114">El parámetro contiene un valor de entrada antes de que se llame al método y un valor de salida cuando devuelve.</span><span class="sxs-lookup"><span data-stu-id="55b77-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55b77-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b77-115">Requirements</span></span>



| <span data-ttu-id="55b77-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b77-116">Requirement</span></span> | <span data-ttu-id="55b77-117">Value</span><span class="sxs-lookup"><span data-stu-id="55b77-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b77-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55b77-118">Header</span></span><br/> | <dl> <span data-ttu-id="55b77-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b77-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

