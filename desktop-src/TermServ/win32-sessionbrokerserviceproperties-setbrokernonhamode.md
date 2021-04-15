---
title: Método SetBrokerNonHAMode de la clase Win32_SessionBrokerServiceProperties
description: Migra datos de la SQL Server central a una base de datos local. También configura el servidor de agente para usar la base de datos local.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Método SetBrokerNonHAMode Servicios de Escritorio remoto
- Método SetBrokerNonHAMode Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685975"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="74403-107">Método SetBrokerNonHAMode de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="74403-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="74403-108">Migra datos de la SQL Server central a una base de datos local.</span><span class="sxs-lookup"><span data-stu-id="74403-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="74403-109">También configura el servidor de agente para usar la base de datos local.</span><span class="sxs-lookup"><span data-stu-id="74403-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="74403-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74403-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="74403-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74403-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74403-112">*connStringToCentralDBRdcms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74403-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74403-113">Cadena de conexión a la base de datos central.</span><span class="sxs-lookup"><span data-stu-id="74403-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74403-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74403-114">Requirements</span></span>



| <span data-ttu-id="74403-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74403-115">Requirement</span></span> | <span data-ttu-id="74403-116">Value</span><span class="sxs-lookup"><span data-stu-id="74403-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74403-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74403-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74403-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="74403-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="74403-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74403-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74403-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74403-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="74403-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74403-121">Namespace</span></span><br/>                | <span data-ttu-id="74403-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="74403-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="74403-123">MOF</span><span class="sxs-lookup"><span data-stu-id="74403-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74403-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74403-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="74403-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74403-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74403-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74403-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74403-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="74403-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74403-128">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="74403-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





