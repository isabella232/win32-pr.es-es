---
title: Método SetStringProperty de la clase Win32_RDMSDeploymentSettings (CertEnroll. h)
description: Actualiza una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Servicios de Escritorio remoto
- Método SetStringProperty Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150594"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="d481f-106">Método SetStringProperty de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="d481f-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="d481f-107">Actualiza una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="d481f-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d481f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d481f-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="d481f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d481f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d481f-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d481f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d481f-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="d481f-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="d481f-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d481f-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d481f-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d481f-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d481f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d481f-114">Requirements</span></span>



| <span data-ttu-id="d481f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d481f-115">Requirement</span></span> | <span data-ttu-id="d481f-116">Value</span><span class="sxs-lookup"><span data-stu-id="d481f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d481f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d481f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d481f-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d481f-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d481f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d481f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d481f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d481f-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d481f-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d481f-121">Namespace</span></span><br/>                | <span data-ttu-id="d481f-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="d481f-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d481f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d481f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d481f-124"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="d481f-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="d481f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d481f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d481f-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d481f-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d481f-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d481f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d481f-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d481f-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d481f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d481f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d481f-130">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="d481f-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





