---
title: Método GetInt32Property de la clase Win32_RDSHCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera un valor de propiedad de entero de un \_ objeto RDSHCollection de Win32.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801454"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="c0029-106">Método GetInt32Property de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="c0029-106">GetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="c0029-107">Recupera un valor de propiedad de entero de un [**objeto \_ RDSHCollection de Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c0029-107">Retrieves an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0029-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0029-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="c0029-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0029-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0029-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c0029-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0029-111">Clave que identifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c0029-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c0029-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c0029-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0029-113">Recibe el valor de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="c0029-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0029-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0029-114">Return value</span></span>

<span data-ttu-id="c0029-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="c0029-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0029-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0029-116">Requirements</span></span>



| <span data-ttu-id="c0029-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0029-117">Requirement</span></span> | <span data-ttu-id="c0029-118">Value</span><span class="sxs-lookup"><span data-stu-id="c0029-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0029-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0029-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0029-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c0029-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="c0029-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0029-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0029-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0029-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="c0029-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0029-123">Namespace</span></span><br/>                | <span data-ttu-id="c0029-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="c0029-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="c0029-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0029-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0029-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0029-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="c0029-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c0029-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0029-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0029-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="c0029-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0029-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0029-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0029-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="c0029-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0029-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0029-132">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="c0029-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





