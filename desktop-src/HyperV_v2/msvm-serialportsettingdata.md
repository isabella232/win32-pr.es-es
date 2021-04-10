---
description: Describe los datos de configuración para un puerto serie virtual.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Msvm_SerialPortSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910130"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="bba76-103">MSVM \_ SerialPortSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="bba76-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="bba76-104">Describe los datos de configuración para un puerto serie virtual.</span><span class="sxs-lookup"><span data-stu-id="bba76-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="bba76-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bba76-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba76-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bba76-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="bba76-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bba76-107">Members</span></span>

<span data-ttu-id="bba76-108">La clase **MSVM \_ SerialPortSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bba76-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bba76-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bba76-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bba76-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bba76-110">Properties</span></span>

<span data-ttu-id="bba76-111">La clase **MSVM \_ SerialPortSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bba76-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bba76-112">**DebuggerMode**</span><span class="sxs-lookup"><span data-stu-id="bba76-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba76-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bba76-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba76-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bba76-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bba76-115">**true** si el modo del depurador está habilitado en un puerto serie virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bba76-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="bba76-116">El modo de depurador mejora el uso de un depurador del kernel de Microsoft Windows a través de un puerto serie virtual.</span><span class="sxs-lookup"><span data-stu-id="bba76-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bba76-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba76-117">Requirements</span></span>



| <span data-ttu-id="bba76-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba76-118">Requirement</span></span> | <span data-ttu-id="bba76-119">Value</span><span class="sxs-lookup"><span data-stu-id="bba76-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba76-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bba76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bba76-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="bba76-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bba76-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bba76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bba76-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bba76-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bba76-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bba76-124">Namespace</span></span><br/>                | <span data-ttu-id="bba76-125">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bba76-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bba76-126">MOF</span><span class="sxs-lookup"><span data-stu-id="bba76-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba76-127"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bba76-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba76-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bba76-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba76-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bba76-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bba76-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bba76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba76-131">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="bba76-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




