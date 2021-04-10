---
title: Método SetStringProperty de la clase Win32_RDSHServer (CertEnroll. h)
description: Actualiza un valor de propiedad de cadena de un \_ objeto RDSHServer de Win32.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Servicios de Escritorio remoto
- Método SetStringProperty Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150592"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="b7983-106">Método SetStringProperty de la \_ clase RDSHServer de Win32</span><span class="sxs-lookup"><span data-stu-id="b7983-106">SetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="b7983-107">Actualiza un valor de propiedad de cadena de un objeto [**\_ RDSHServer de Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b7983-107">Updates a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7983-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7983-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="b7983-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7983-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7983-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b7983-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7983-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="b7983-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="b7983-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b7983-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7983-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7983-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7983-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7983-114">Return value</span></span>

<span data-ttu-id="b7983-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b7983-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7983-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7983-116">Requirements</span></span>



| <span data-ttu-id="b7983-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7983-117">Requirement</span></span> | <span data-ttu-id="b7983-118">Value</span><span class="sxs-lookup"><span data-stu-id="b7983-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7983-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7983-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7983-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b7983-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b7983-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7983-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7983-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7983-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b7983-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7983-123">Namespace</span></span><br/>                | <span data-ttu-id="b7983-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="b7983-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b7983-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7983-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7983-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="b7983-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b7983-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7983-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7983-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7983-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7983-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b7983-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7983-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7983-132">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="b7983-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





