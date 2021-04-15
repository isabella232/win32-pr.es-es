---
title: Método GetStringProperty de la clase Win32_RDMSVirtualDesktopCollection
description: Recupera una propiedad de cadena de una colección de escritorios virtuales.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676600"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="3e7e0-106">Método GetStringProperty de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="3e7e0-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="3e7e0-107">Recupera una propiedad de cadena de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="3e7e0-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e7e0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e7e0-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="3e7e0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e7e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e7e0-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3e7e0-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e7e0-111">Clave que identifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3e7e0-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3e7e0-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3e7e0-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e7e0-113">Cadena que recibe el valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="3e7e0-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e7e0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e7e0-114">Return value</span></span>

<span data-ttu-id="3e7e0-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e7e0-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e7e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e7e0-116">Requirements</span></span>



| <span data-ttu-id="3e7e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e7e0-117">Requirement</span></span> | <span data-ttu-id="3e7e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="3e7e0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7e0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e7e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7e0-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e7e0-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3e7e0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e7e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7e0-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e7e0-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3e7e0-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e7e0-123">Namespace</span></span><br/>                | <span data-ttu-id="3e7e0-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="3e7e0-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3e7e0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3e7e0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e7e0-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e7e0-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e7e0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e7e0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e7e0-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e7e0-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3e7e0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e7e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e7e0-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="3e7e0-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





