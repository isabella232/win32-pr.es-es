---
title: Método SetBrokerHAMode de la clase Win32_SessionBrokerServiceProperties
description: Migra datos de una base de datos WID local a la nueva base de datos basada en SQL Server. También configura el servidor de agente para usar SQL Server central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Método SetBrokerHAMode Servicios de Escritorio remoto
- Método SetBrokerHAMode Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150283"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="805e7-107">Método SetBrokerHAMode de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="805e7-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="805e7-108">Migra datos de una base de datos WID local a la nueva base de datos basada en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="805e7-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="805e7-109">También configura el servidor de agente para usar SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="805e7-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="805e7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="805e7-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="805e7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="805e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805e7-112">*connStringToCentralDBRdcms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="805e7-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805e7-113">Cadena de conexión a la base de datos central.</span><span class="sxs-lookup"><span data-stu-id="805e7-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="805e7-114">*secondaryConnStringToCentralDBRdcms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="805e7-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805e7-115">Cadena de conexión secundaria a la base de datos central.</span><span class="sxs-lookup"><span data-stu-id="805e7-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="805e7-116">**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="805e7-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="805e7-117">*brokerDnsRRName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="805e7-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805e7-118">Nombre DNS del agente.</span><span class="sxs-lookup"><span data-stu-id="805e7-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="805e7-119">*activeBrokerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="805e7-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805e7-120">Nombre del agente activo.</span><span class="sxs-lookup"><span data-stu-id="805e7-120">Active broker name.</span></span>

<span data-ttu-id="805e7-121">**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="805e7-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="805e7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805e7-122">Requirements</span></span>



| <span data-ttu-id="805e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="805e7-123">Requirement</span></span> | <span data-ttu-id="805e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="805e7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="805e7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="805e7-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="805e7-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="805e7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="805e7-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="805e7-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="805e7-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="805e7-129">Namespace</span></span><br/>                | <span data-ttu-id="805e7-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="805e7-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="805e7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="805e7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="805e7-132"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="805e7-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="805e7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="805e7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805e7-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805e7-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805e7-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="805e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805e7-136">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="805e7-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





