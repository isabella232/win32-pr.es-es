---
title: Método KeyValueGet de la clase Win32_RDSHCollection
description: Recupera el valor asociado a la clave especificada de la colección.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Método KeyValueGet Servicios de Escritorio remoto
- Método KeyValueGet Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905154"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="e4c5c-106">Método KeyValueGet de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="e4c5c-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="e4c5c-107">Recupera el valor asociado a la clave especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4c5c-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="e4c5c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4c5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c5c-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e4c5c-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c5c-111">Clave que identifica el valor que se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e4c5c-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e4c5c-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c5c-113">Si se ejecuta correctamente, devuelve el valor asociado a la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4c5c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4c5c-114">Requirements</span></span>



| <span data-ttu-id="e4c5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c5c-115">Requirement</span></span> | <span data-ttu-id="e4c5c-116">Value</span><span class="sxs-lookup"><span data-stu-id="e4c5c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c5c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c5c-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e4c5c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e4c5c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c5c-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e4c5c-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e4c5c-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e4c5c-121">Namespace</span></span><br/>                | <span data-ttu-id="e4c5c-122">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="e4c5c-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e4c5c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e4c5c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4c5c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4c5c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4c5c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4c5c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c5c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c5c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e4c5c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4c5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c5c-128">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="e4c5c-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





