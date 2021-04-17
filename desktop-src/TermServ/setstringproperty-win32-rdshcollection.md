---
title: Método SetStringProperty de la clase Win32_RDSHCollection (CertEnroll. h)
description: Actualiza un valor de propiedad de cadena de un \_ objeto RDSHCollection de Win32.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Servicios de Escritorio remoto
- Método SetStringProperty Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676839"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="9d1a9-106">Método SetStringProperty de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="9d1a9-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="9d1a9-107">Actualiza un valor de propiedad de cadena de un objeto [**\_ RDSHCollection de Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="9d1a9-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1a9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d1a9-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="9d1a9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d1a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d1a9-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9d1a9-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d1a9-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="9d1a9-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a9-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9d1a9-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d1a9-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d1a9-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d1a9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d1a9-114">Return value</span></span>

<span data-ttu-id="9d1a9-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="9d1a9-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d1a9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d1a9-116">Requirements</span></span>



| <span data-ttu-id="9d1a9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d1a9-117">Requirement</span></span> | <span data-ttu-id="9d1a9-118">Value</span><span class="sxs-lookup"><span data-stu-id="9d1a9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1a9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1a9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1a9-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9d1a9-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9d1a9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1a9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1a9-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d1a9-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9d1a9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d1a9-123">Namespace</span></span><br/>                | <span data-ttu-id="9d1a9-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="9d1a9-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9d1a9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d1a9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d1a9-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a9-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="9d1a9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9d1a9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d1a9-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a9-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d1a9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d1a9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1a9-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a9-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9d1a9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d1a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1a9-132">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="9d1a9-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





