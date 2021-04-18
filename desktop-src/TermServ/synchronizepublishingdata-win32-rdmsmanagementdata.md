---
title: Método SynchronizePublishingData de la clase Win32_RDMSManagementData
description: Sincroniza el conjunto especificado de datos de publicación para Escritorio remoto Management Services (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Método SynchronizePublishingData Servicios de Escritorio remoto
- Método SynchronizePublishingData Servicios de Escritorio remoto, clase Win32_RDMSManagementData
- Win32_RDMSManagementData de clase Servicios de Escritorio remoto, método SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422262"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="b1208-106">Método SynchronizePublishingData de la \_ clase RDMSManagementData de Win32</span><span class="sxs-lookup"><span data-stu-id="b1208-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="b1208-107">Sincroniza el conjunto especificado de datos de publicación para Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="b1208-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1208-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1208-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="b1208-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1208-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1208-110">*Contexto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b1208-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1208-111">Información de contexto de los datos de publicación que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="b1208-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1208-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1208-112">Return value</span></span>

<span data-ttu-id="b1208-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b1208-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1208-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1208-114">Requirements</span></span>



| <span data-ttu-id="b1208-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1208-115">Requirement</span></span> | <span data-ttu-id="b1208-116">Value</span><span class="sxs-lookup"><span data-stu-id="b1208-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1208-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1208-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1208-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1208-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b1208-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1208-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1208-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1208-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b1208-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1208-121">Namespace</span></span><br/>                | <span data-ttu-id="b1208-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="b1208-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b1208-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b1208-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1208-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1208-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1208-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1208-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1208-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1208-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b1208-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1208-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1208-128">**Win32 \_ RDMSManagementData**</span><span class="sxs-lookup"><span data-stu-id="b1208-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





