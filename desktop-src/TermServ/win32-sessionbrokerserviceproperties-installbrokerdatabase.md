---
title: Método InstallBrokerDatabase de la clase Win32_SessionBrokerServiceProperties
description: Instala una base de datos de agente de conexión a escritorio remoto en un servidor SQL Server central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Método InstallBrokerDatabase Servicios de Escritorio remoto
- Método InstallBrokerDatabase Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801298"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="2d3ea-106">Método InstallBrokerDatabase de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="2d3ea-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="2d3ea-107">Instala una base de datos de agente de conexión a escritorio remoto en un servidor SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3ea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d3ea-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="2d3ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d3ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3ea-110">*newDbFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d3ea-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3ea-111">nueva ruta de acceso del archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="2d3ea-112">*connStringToCentralDBMaster* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d3ea-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3ea-113">Cadena de conexión al maestro de base de datos central.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="2d3ea-114">*centralRdcmsDbName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d3ea-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3ea-115">Nombre de la base de datos central.</span><span class="sxs-lookup"><span data-stu-id="2d3ea-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d3ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d3ea-116">Requirements</span></span>



| <span data-ttu-id="2d3ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d3ea-117">Requirement</span></span> | <span data-ttu-id="2d3ea-118">Value</span><span class="sxs-lookup"><span data-stu-id="2d3ea-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3ea-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d3ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3ea-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2d3ea-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2d3ea-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d3ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3ea-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d3ea-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2d3ea-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d3ea-123">Namespace</span></span><br/>                | <span data-ttu-id="2d3ea-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2d3ea-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="2d3ea-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2d3ea-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d3ea-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d3ea-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d3ea-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d3ea-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d3ea-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d3ea-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3ea-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d3ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3ea-130">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="2d3ea-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





