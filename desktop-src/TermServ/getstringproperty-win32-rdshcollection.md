---
title: Método GetStringProperty de la clase Win32_RDSHCollection
description: Recupera un valor de propiedad de cadena de un \_ objeto RDSHCollection de Win32.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996081"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="dea06-106">Método GetStringProperty de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="dea06-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="dea06-107">Recupera un valor de propiedad de cadena de un objeto [**\_ RDSHCollection de Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="dea06-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea06-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dea06-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="dea06-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dea06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea06-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dea06-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea06-111">Clave que identifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="dea06-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dea06-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dea06-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea06-113">Recibe el valor de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="dea06-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea06-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dea06-114">Return value</span></span>

<span data-ttu-id="dea06-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="dea06-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea06-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea06-116">Requirements</span></span>



| <span data-ttu-id="dea06-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea06-117">Requirement</span></span> | <span data-ttu-id="dea06-118">Value</span><span class="sxs-lookup"><span data-stu-id="dea06-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea06-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea06-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dea06-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dea06-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dea06-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea06-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dea06-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dea06-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="dea06-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dea06-123">Namespace</span></span><br/>                | <span data-ttu-id="dea06-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="dea06-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dea06-125">MOF</span><span class="sxs-lookup"><span data-stu-id="dea06-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dea06-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dea06-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dea06-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dea06-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea06-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea06-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dea06-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dea06-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea06-130">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="dea06-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





