---
title: Tipos de datos simples de ADSI (iAds. h)
description: Active Directory interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079010"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="66888-114">Tipos de datos simples de ADSI</span><span class="sxs-lookup"><span data-stu-id="66888-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="66888-115">Active Directory interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.</span><span class="sxs-lookup"><span data-stu-id="66888-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="66888-116">**ADS \_ booleano**</span><span class="sxs-lookup"><span data-stu-id="66888-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="66888-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="66888-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="66888-118">**\_ \_ cadena exacta de caso de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="66888-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-120">**caso de ADS \_ \_ omitir \_ cadena**</span><span class="sxs-lookup"><span data-stu-id="66888-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="66888-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-122">**\_cadena DN de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="66888-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-124">**entero de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="66888-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="66888-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="66888-126">**\_entero grande de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="66888-127">**\_entero grande**</span><span class="sxs-lookup"><span data-stu-id="66888-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="66888-128">**\_cadena numérica de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="66888-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-130">**\_clase de objeto ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="66888-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-132">**\_cadena imprimible de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="66888-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66888-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="66888-134">**\_identificador de búsqueda de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="66888-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="66888-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="66888-136">**\_hora UTC de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="66888-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="66888-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="66888-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66888-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66888-138">Remarks</span></span>

<span data-ttu-id="66888-139">Cuando ADSI Lee un atributo que se ha definido como un **entero** en el esquema LDAP, siempre controlará el entero como un valor de 32 bits y puede truncar los datos.</span><span class="sxs-lookup"><span data-stu-id="66888-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="66888-140">Esto solo es un problema para los servidores LDAP que permiten valores enteros de tamaño arbitrario.</span><span class="sxs-lookup"><span data-stu-id="66888-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="66888-141">Si el atributo es un atributo personalizado que se define extendiendo el esquema, este problema se puede evitar definiendo el atributo personalizado como una cadena.</span><span class="sxs-lookup"><span data-stu-id="66888-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="66888-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66888-142">Requirements</span></span>



| <span data-ttu-id="66888-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="66888-143">Requirement</span></span> | <span data-ttu-id="66888-144">Value</span><span class="sxs-lookup"><span data-stu-id="66888-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="66888-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66888-145">Minimum supported client</span></span><br/> | <span data-ttu-id="66888-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66888-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="66888-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66888-147">Minimum supported server</span></span><br/> | <span data-ttu-id="66888-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66888-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="66888-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66888-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="66888-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="66888-150"><dt>Iads.h</dt></span></span> </dl> |



 

