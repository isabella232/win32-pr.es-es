---
title: Método KeyValueCompareAndSet de la clase Win32_RDSHCollection
description: Compara la clave especificada de la colección con un comparand; Si coinciden, la clave se establece en un valor nuevo. Si la clave no existe, el método insertará la clave en la colección.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Método KeyValueCompareAndSet Servicios de Escritorio remoto
- Método KeyValueCompareAndSet Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905155"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="60656-107">Método KeyValueCompareAndSet de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="60656-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="60656-108">Compara la clave especificada de la colección con un comparand; Si coinciden, la clave se establece en un valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="60656-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="60656-109">Si la clave no existe, el método insertará la clave en la colección.</span><span class="sxs-lookup"><span data-stu-id="60656-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60656-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60656-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="60656-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60656-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60656-112">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="60656-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60656-113">Clave que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="60656-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="60656-114">*Nuevovalor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60656-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60656-115">Nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="60656-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="60656-116">*Comparand* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60656-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60656-117">Cadena a la que se va a comparar la clave.</span><span class="sxs-lookup"><span data-stu-id="60656-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="60656-118">*InitialValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60656-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60656-119">En caso de éxito o error, contiene el valor inicial de la clave.</span><span class="sxs-lookup"><span data-stu-id="60656-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60656-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60656-120">Remarks</span></span>

<span data-ttu-id="60656-121">Tenga en cuenta que este método puede recuperar el valor de la clave y, como tal, encapsula la funcionalidad de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span><span class="sxs-lookup"><span data-stu-id="60656-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60656-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60656-122">Requirements</span></span>



| <span data-ttu-id="60656-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60656-123">Requirement</span></span> | <span data-ttu-id="60656-124">Value</span><span class="sxs-lookup"><span data-stu-id="60656-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60656-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60656-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60656-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60656-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="60656-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60656-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60656-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60656-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="60656-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60656-129">Namespace</span></span><br/>                | <span data-ttu-id="60656-130">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="60656-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="60656-131">MOF</span><span class="sxs-lookup"><span data-stu-id="60656-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60656-132"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60656-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="60656-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60656-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60656-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60656-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="60656-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="60656-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60656-136">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="60656-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





