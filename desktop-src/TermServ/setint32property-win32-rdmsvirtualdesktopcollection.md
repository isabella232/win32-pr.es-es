---
title: Método SetInt32Property de la clase Win32_RDMSVirtualDesktopCollection
description: Actualiza una propiedad de entero de una colección de escritorios virtuales.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151007"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="62911-106">Método SetInt32Property de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="62911-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="62911-107">Actualiza una propiedad de entero de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="62911-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="62911-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62911-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="62911-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62911-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62911-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="62911-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62911-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="62911-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="62911-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="62911-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62911-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="62911-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62911-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62911-114">Return value</span></span>

<span data-ttu-id="62911-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="62911-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62911-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62911-116">Requirements</span></span>



| <span data-ttu-id="62911-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="62911-117">Requirement</span></span> | <span data-ttu-id="62911-118">Value</span><span class="sxs-lookup"><span data-stu-id="62911-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="62911-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62911-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62911-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62911-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="62911-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62911-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62911-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62911-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="62911-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62911-123">Namespace</span></span><br/>                | <span data-ttu-id="62911-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="62911-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="62911-125">MOF</span><span class="sxs-lookup"><span data-stu-id="62911-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62911-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62911-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="62911-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62911-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62911-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62911-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="62911-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="62911-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62911-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="62911-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





