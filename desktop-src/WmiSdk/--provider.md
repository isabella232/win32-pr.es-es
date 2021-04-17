---
description: Actúa como la clase primaria de la \_ \_ clase del sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716217"
---
# <a name="__provider-class"></a><span data-ttu-id="1e7d1-103">\_\_Provider (clase)</span><span class="sxs-lookup"><span data-stu-id="1e7d1-103">\_\_Provider class</span></span>

<span data-ttu-id="1e7d1-104">La clase de sistema de **\_ \_ proveedor** es una clase base abstracta que actúa como la clase primaria de la clase del sistema [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="1e7d1-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="1e7d1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1e7d1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e7d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e7d1-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="1e7d1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e7d1-108">Members</span></span>

<span data-ttu-id="1e7d1-109">La clase de **\_ \_ proveedor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e7d1-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="1e7d1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e7d1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e7d1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e7d1-111">Properties</span></span>

<span data-ttu-id="1e7d1-112">La clase de **\_ \_ proveedor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e7d1-113">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1e7d1-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e7d1-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e7d1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e7d1-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e7d1-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e7d1-116">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1e7d1-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1e7d1-117">Cadena independiente del lenguaje que identifica de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="1e7d1-118">Se sugiere el siguiente formato para evitar conflictos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="1e7d1-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="1e7d1-119">\|versión del proveedor del proveedor \|</span><span class="sxs-lookup"><span data-stu-id="1e7d1-119">vendor\|provider\|version</span></span>

<span data-ttu-id="1e7d1-120">Por ejemplo, este nombre de proveedor representa la versión 1,0 de Microsoft TestProvider:</span><span class="sxs-lookup"><span data-stu-id="1e7d1-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="1e7d1-121">"Microsoft \| TestProvider \| v 1.0"</span><span class="sxs-lookup"><span data-stu-id="1e7d1-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e7d1-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e7d1-122">Remarks</span></span>

<span data-ttu-id="1e7d1-123">La clase de **\_ \_ proveedor** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="1e7d1-124">Los proveedores crean instancias de [**\_ \_ Win32Provider**](--win32provider.md) para especificar información sobre su implementación física.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7d1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e7d1-125">Requirements</span></span>



| <span data-ttu-id="1e7d1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e7d1-126">Requirement</span></span> | <span data-ttu-id="1e7d1-127">Value</span><span class="sxs-lookup"><span data-stu-id="1e7d1-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1e7d1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e7d1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7d1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e7d1-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1e7d1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e7d1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7d1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e7d1-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1e7d1-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e7d1-132">Namespace</span></span><br/>                | <span data-ttu-id="1e7d1-133">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="1e7d1-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1e7d1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e7d1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7d1-135">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="1e7d1-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="1e7d1-136">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1e7d1-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1e7d1-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="1e7d1-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

