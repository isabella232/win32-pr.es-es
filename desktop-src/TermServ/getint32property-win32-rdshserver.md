---
title: Método GetInt32Property de la clase Win32_RDSHServer (Microsoft. Diagnostics. appanalysis. h)
description: Recupera un valor de propiedad de entero de un \_ objeto RDSHServer de Win32.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996603"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="f99f1-106">Método GetInt32Property de la \_ clase RDSHServer de Win32</span><span class="sxs-lookup"><span data-stu-id="f99f1-106">GetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="f99f1-107">Recupera un valor de propiedad de entero de un [**objeto \_ RDSHServer de Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f99f1-107">Retrieves an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99f1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f99f1-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="f99f1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f99f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99f1-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f99f1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99f1-111">Clave que identifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f99f1-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f99f1-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f99f1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f99f1-113">Recibe el valor de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="f99f1-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99f1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f99f1-114">Return value</span></span>

<span data-ttu-id="f99f1-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f99f1-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99f1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f99f1-116">Requirements</span></span>



| <span data-ttu-id="f99f1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f99f1-117">Requirement</span></span> | <span data-ttu-id="f99f1-118">Value</span><span class="sxs-lookup"><span data-stu-id="f99f1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99f1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f99f1-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f99f1-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="f99f1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f99f1-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f99f1-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="f99f1-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f99f1-123">Namespace</span></span><br/>                | <span data-ttu-id="f99f1-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="f99f1-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="f99f1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f99f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f99f1-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="f99f1-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="f99f1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="f99f1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f99f1-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f99f1-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="f99f1-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f99f1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f99f1-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f99f1-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="f99f1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f99f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99f1-132">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="f99f1-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





