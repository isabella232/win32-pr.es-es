---
description: Representa un controlador de protocolo que administra una interfaz SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686903"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="35402-103">\_Clase SCSIProtocolController de CIM</span><span class="sxs-lookup"><span data-stu-id="35402-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="35402-104">Representa un controlador de protocolo que administra una interfaz SCSI.</span><span class="sxs-lookup"><span data-stu-id="35402-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="35402-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35402-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="35402-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="35402-106">Members</span></span>

<span data-ttu-id="35402-107">La clase **CIM \_ SCSIProtocolController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35402-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="35402-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35402-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35402-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35402-109">Properties</span></span>

<span data-ttu-id="35402-110">La clase **CIM \_ SCSIProtocolController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35402-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35402-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="35402-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35402-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35402-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35402-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35402-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35402-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="35402-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="35402-115">El formato de la propiedad **Name** de la **\_ SCSIProtocolController CIM**.</span><span class="sxs-lookup"><span data-stu-id="35402-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35402-116">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="35402-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="35402-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="35402-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="35402-118">**WWN del puerto FC** (2)</span><span class="sxs-lookup"><span data-stu-id="35402-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="35402-119">**nombre iSCSI** (3)</span><span class="sxs-lookup"><span data-stu-id="35402-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35402-120">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="35402-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35402-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35402-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35402-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35402-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35402-123">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="35402-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="35402-124">Una descripción de la propiedad **nameFormat** cuando **NameFormat** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="35402-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35402-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35402-125">Requirements</span></span>



| <span data-ttu-id="35402-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="35402-126">Requirement</span></span> | <span data-ttu-id="35402-127">Value</span><span class="sxs-lookup"><span data-stu-id="35402-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35402-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35402-128">Minimum supported client</span></span><br/> | <span data-ttu-id="35402-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="35402-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="35402-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35402-130">Minimum supported server</span></span><br/> | <span data-ttu-id="35402-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35402-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="35402-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35402-132">Namespace</span></span><br/>                | <span data-ttu-id="35402-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="35402-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35402-134">MOF</span><span class="sxs-lookup"><span data-stu-id="35402-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35402-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35402-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35402-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35402-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35402-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35402-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35402-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="35402-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35402-139">**\_PROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="35402-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

