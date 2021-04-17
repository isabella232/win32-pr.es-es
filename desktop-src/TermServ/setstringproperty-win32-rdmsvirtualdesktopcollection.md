---
title: Método SetStringProperty de la clase Win32_RDMSVirtualDesktopCollection (CertEnroll. h)
description: Actualiza una propiedad de cadena de una colección de escritorios virtuales.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Servicios de Escritorio remoto
- Método SetStringProperty Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676840"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="44e71-106">Método SetStringProperty de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="44e71-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="44e71-107">Actualiza una propiedad de cadena de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="44e71-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44e71-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="44e71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44e71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44e71-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="44e71-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44e71-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="44e71-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="44e71-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="44e71-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44e71-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="44e71-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44e71-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44e71-114">Return value</span></span>

<span data-ttu-id="44e71-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="44e71-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e71-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e71-116">Requirements</span></span>



| <span data-ttu-id="44e71-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e71-117">Requirement</span></span> | <span data-ttu-id="44e71-118">Value</span><span class="sxs-lookup"><span data-stu-id="44e71-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e71-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e71-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44e71-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44e71-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="44e71-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e71-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44e71-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44e71-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="44e71-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44e71-123">Namespace</span></span><br/>                | <span data-ttu-id="44e71-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="44e71-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="44e71-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44e71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e71-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e71-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="44e71-127">MOF</span><span class="sxs-lookup"><span data-stu-id="44e71-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44e71-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44e71-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="44e71-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44e71-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44e71-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e71-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="44e71-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="44e71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e71-132">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="44e71-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





