---
description: Registra proveedores de métodos con WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707109"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="7ec31-103">\_\_Clase MethodProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="7ec31-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="7ec31-104">La clase del sistema **\_ \_ MethodProviderRegistration** registra los proveedores de métodos con WMI.</span><span class="sxs-lookup"><span data-stu-id="7ec31-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="7ec31-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7ec31-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7ec31-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7ec31-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ec31-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="7ec31-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ec31-108">Members</span></span>

<span data-ttu-id="7ec31-109">La clase **\_ \_ MethodProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ec31-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="7ec31-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ec31-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ec31-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ec31-111">Properties</span></span>

<span data-ttu-id="7ec31-112">La clase **\_ \_ MethodProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ec31-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ec31-113">**presta**</span><span class="sxs-lookup"><span data-stu-id="7ec31-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ec31-114">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="7ec31-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="7ec31-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ec31-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ec31-116">Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa la ruta de acceso del objeto del proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="7ec31-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="7ec31-117">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7ec31-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ec31-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ec31-118">Remarks</span></span>

<span data-ttu-id="7ec31-119">La clase **\_ \_ MethodProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7ec31-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="7ec31-120">Solo los administradores pueden registrar o eliminar un proveedor de métodos mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ MethodProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="7ec31-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec31-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ec31-121">Requirements</span></span>



| <span data-ttu-id="7ec31-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec31-122">Requirement</span></span> | <span data-ttu-id="7ec31-123">Value</span><span class="sxs-lookup"><span data-stu-id="7ec31-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7ec31-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ec31-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec31-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ec31-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7ec31-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ec31-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec31-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ec31-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7ec31-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7ec31-128">Namespace</span></span><br/>                | <span data-ttu-id="7ec31-129">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="7ec31-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7ec31-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ec31-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec31-131">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7ec31-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="7ec31-132">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="7ec31-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7ec31-133">Registrar un proveedor de métodos</span><span class="sxs-lookup"><span data-stu-id="7ec31-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

