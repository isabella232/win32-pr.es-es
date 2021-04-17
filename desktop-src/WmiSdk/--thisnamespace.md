---
description: Contiene los derechos de seguridad para el espacio de nombres en forma de un descriptor de seguridad.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688246"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="9f28d-103">\_\_clase thisNAMESPACE</span><span class="sxs-lookup"><span data-stu-id="9f28d-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="9f28d-104">La clase del sistema **\_ \_ thisNAMESPACE** contiene los derechos de seguridad para el espacio de nombres en forma de un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9f28d-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="9f28d-105">Esta clase y una sola instancia se encuentran en todos los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="9f28d-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="9f28d-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9f28d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9f28d-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9f28d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f28d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f28d-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="9f28d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f28d-109">Members</span></span>

<span data-ttu-id="9f28d-110">La clase **\_ \_ thisNAMESPACE** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f28d-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="9f28d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f28d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f28d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f28d-112">Properties</span></span>

<span data-ttu-id="9f28d-113">La clase **\_ \_ thisNAMESPACE** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f28d-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f28d-114">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="9f28d-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f28d-115">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="9f28d-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9f28d-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f28d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f28d-117">Descriptor de seguridad que describe quién puede tener acceso al espacio de nombres y quién puede leer o escribir en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9f28d-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="9f28d-118">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="9f28d-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="9f28d-119">Para obtener más información sobre el formato de los descriptores de seguridad, consulte [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors) en la sección seguridad de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9f28d-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f28d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f28d-120">Remarks</span></span>

<span data-ttu-id="9f28d-121">La instancia singleton de **\_ \_ thisNAMESPACE** es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f28d-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="9f28d-122">Para cambiar la configuración de la propiedad del descriptor de seguridad, use los métodos de la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="9f28d-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="9f28d-123">La clase **\_ \_ thisNAMESPACE** se deriva de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="9f28d-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f28d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f28d-124">Requirements</span></span>



| <span data-ttu-id="9f28d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f28d-125">Requirement</span></span> | <span data-ttu-id="9f28d-126">Value</span><span class="sxs-lookup"><span data-stu-id="9f28d-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9f28d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f28d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9f28d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f28d-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9f28d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f28d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9f28d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f28d-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="9f28d-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f28d-131">Namespace</span></span><br/>                | <span data-ttu-id="9f28d-132">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="9f28d-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="9f28d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f28d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f28d-134">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="9f28d-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="9f28d-135">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="9f28d-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

