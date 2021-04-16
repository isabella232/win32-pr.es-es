---
title: Métodos de la propiedad IADsReplicaPointer (iAds. h)
description: El método Property de la interfaz IADsReplicaPointer establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsReplicaPointer ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534048"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="827aa-105">Métodos de propiedad IADsReplicaPointer</span><span class="sxs-lookup"><span data-stu-id="827aa-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="827aa-106">El método Property de la interfaz [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="827aa-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="827aa-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="827aa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="827aa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="827aa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="827aa-109">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="827aa-109">**Count**</span></span>
<span data-ttu-id="827aa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="827aa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="827aa-111">El número de réplicas existentes.</span><span class="sxs-lookup"><span data-stu-id="827aa-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="827aa-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="827aa-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="827aa-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="827aa-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="827aa-114">**ReplicaAddressHints**</span><span class="sxs-lookup"><span data-stu-id="827aa-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="827aa-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="827aa-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="827aa-116">Una dirección de red sugerida como referencia probable a un nodo que conduce al servidor de nombres.</span><span class="sxs-lookup"><span data-stu-id="827aa-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="827aa-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="827aa-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="827aa-118">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="827aa-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="827aa-119">**ReplicaNumber**</span><span class="sxs-lookup"><span data-stu-id="827aa-119">**ReplicaNumber**</span></span>
<span data-ttu-id="827aa-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="827aa-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="827aa-121">Número de identificación de la réplica.</span><span class="sxs-lookup"><span data-stu-id="827aa-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="827aa-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="827aa-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="827aa-123">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="827aa-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="827aa-124">**ReplicaType**</span><span class="sxs-lookup"><span data-stu-id="827aa-124">**ReplicaType**</span></span>
<span data-ttu-id="827aa-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="827aa-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="827aa-126">Tipo de réplica (principal, secundaria o de solo lectura).</span><span class="sxs-lookup"><span data-stu-id="827aa-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="827aa-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="827aa-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="827aa-128">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="827aa-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="827aa-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="827aa-129">**ServerName**</span></span>
<span data-ttu-id="827aa-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="827aa-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="827aa-131">Nombre del servidor de nombres que contiene la réplica.</span><span class="sxs-lookup"><span data-stu-id="827aa-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="827aa-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="827aa-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="827aa-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="827aa-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="827aa-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="827aa-134">Requirements</span></span>



| <span data-ttu-id="827aa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="827aa-135">Requirement</span></span> | <span data-ttu-id="827aa-136">Value</span><span class="sxs-lookup"><span data-stu-id="827aa-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="827aa-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="827aa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="827aa-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="827aa-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="827aa-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="827aa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="827aa-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="827aa-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="827aa-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="827aa-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="827aa-142"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="827aa-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="827aa-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="827aa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="827aa-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="827aa-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="827aa-145">IID</span><span class="sxs-lookup"><span data-stu-id="827aa-145">IID</span></span><br/>                      | <span data-ttu-id="827aa-146">IID \_ IADsReplicaPointer se define como F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="827aa-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="827aa-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="827aa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827aa-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="827aa-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="827aa-149">**\_REPLICAPOINTER ADS**</span><span class="sxs-lookup"><span data-stu-id="827aa-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





