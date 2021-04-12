---
description: Contiene el tipo de conexión del monitor.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Clase WmiMonitorConnectionParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277711"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="4b23b-103">Clase WmiMonitorConnectionParams</span><span class="sxs-lookup"><span data-stu-id="4b23b-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="4b23b-104">La clase WMI WmiMonitorConnectionParams contiene el tipo de conexión del monitor.</span><span class="sxs-lookup"><span data-stu-id="4b23b-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="4b23b-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4b23b-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b23b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b23b-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="4b23b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b23b-107">Members</span></span>

<span data-ttu-id="4b23b-108">La clase **WmiMonitorConnectionParams** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4b23b-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="4b23b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b23b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b23b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b23b-110">Properties</span></span>

<span data-ttu-id="4b23b-111">La clase **WmiMonitorConnectionParams** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4b23b-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b23b-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="4b23b-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b23b-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4b23b-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b23b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4b23b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b23b-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="4b23b-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4b23b-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4b23b-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b23b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4b23b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b23b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4b23b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b23b-119">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4b23b-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4b23b-120">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="4b23b-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="4b23b-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="4b23b-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b23b-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b23b-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b23b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4b23b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b23b-124">Tipo de conexión de tecnología de salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4b23b-124">Video output technology connection type.</span></span> <span data-ttu-id="4b23b-125">Los valores válidos se documentan en la enumeración [ \_ tecnología de \_ salida \_ de vídeo D3DKMDT](https://msdn.microsoft.com/library/ms794498.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b23b-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](https://msdn.microsoft.com/library/ms794498.aspx) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b23b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b23b-126">Requirements</span></span>



| <span data-ttu-id="4b23b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b23b-127">Requirement</span></span> | <span data-ttu-id="4b23b-128">Value</span><span class="sxs-lookup"><span data-stu-id="4b23b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b23b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b23b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4b23b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b23b-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b23b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b23b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4b23b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b23b-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b23b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b23b-133">Namespace</span></span><br/>                | <span data-ttu-id="4b23b-134">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="4b23b-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4b23b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4b23b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b23b-136"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b23b-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b23b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b23b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b23b-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b23b-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b23b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b23b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b23b-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="4b23b-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




