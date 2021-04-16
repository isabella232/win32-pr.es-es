---
title: Método IsDbReachable de la clase Win32_SessionBrokerServiceProperties
description: Comprueba si la base de datos es accesible.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Método IsDbReachable Servicios de Escritorio remoto
- Método IsDbReachable Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490582"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="073ac-106">Método IsDbReachable de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="073ac-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="073ac-107">Comprueba si la base de datos es accesible.</span><span class="sxs-lookup"><span data-stu-id="073ac-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="073ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="073ac-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="073ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="073ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073ac-110">*connStringToDb* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073ac-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073ac-111">La cadena de conexión a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="073ac-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="073ac-112">*connSecondaryStringToDb* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073ac-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073ac-113">Cadena de conexión secundaria a la base de datos central.</span><span class="sxs-lookup"><span data-stu-id="073ac-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="073ac-114">**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="073ac-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="073ac-115">*activeBrokerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073ac-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073ac-116">Nombre del agente activo.</span><span class="sxs-lookup"><span data-stu-id="073ac-116">Active broker name.</span></span>

<span data-ttu-id="073ac-117">**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="073ac-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="073ac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="073ac-118">Requirements</span></span>



| <span data-ttu-id="073ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="073ac-119">Requirement</span></span> | <span data-ttu-id="073ac-120">Value</span><span class="sxs-lookup"><span data-stu-id="073ac-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="073ac-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="073ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="073ac-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="073ac-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="073ac-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="073ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="073ac-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="073ac-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="073ac-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="073ac-125">Namespace</span></span><br/>                | <span data-ttu-id="073ac-126">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="073ac-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="073ac-127">MOF</span><span class="sxs-lookup"><span data-stu-id="073ac-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="073ac-128"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="073ac-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="073ac-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="073ac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="073ac-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="073ac-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="073ac-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="073ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073ac-132">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="073ac-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





