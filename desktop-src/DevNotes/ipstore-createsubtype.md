---
description: Crea el subtipo especificado en el tipo especificado.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'IPStore:: CreateSubtype (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649564"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="2ffc0-103">IPStore:: CreateSubtype (método)</span><span class="sxs-lookup"><span data-stu-id="2ffc0-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="2ffc0-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2ffc0-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2ffc0-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2ffc0-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2ffc0-108">Crea el subtipo especificado en el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffc0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ffc0-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2ffc0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ffc0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ffc0-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-112">Especifica el área de almacenamiento del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="2ffc0-113">Value</span><span class="sxs-lookup"><span data-stu-id="2ffc0-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="2ffc0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2ffc0-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="2ffc0-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2ffc0-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="2ffc0-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="2ffc0-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2ffc0-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2ffc0-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2ffc0-119">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-120">Un puntero a un **GUID** que identifica el tipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="2ffc0-121">*pSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-122">Un puntero a un **GUID** que identifica el subtipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="2ffc0-123">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-124">Puntero a una estructura [**de \_ TYPEINFO de PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2ffc0-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ffc0-125">*pRules* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-126">Puntero a una estructura [**\_ ACCESSRULESET de PST**](pst-accessruleset.md) .</span><span class="sxs-lookup"><span data-stu-id="2ffc0-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="2ffc0-127">**Windows XP:** Este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ffc0-128">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffc0-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffc0-129">Sector debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ffc0-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ffc0-130">Return value</span></span>

<span data-ttu-id="2ffc0-131">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ffc0-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="2ffc0-132">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ffc0-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ffc0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ffc0-133">Requirements</span></span>



| <span data-ttu-id="2ffc0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ffc0-134">Requirement</span></span> | <span data-ttu-id="2ffc0-135">Value</span><span class="sxs-lookup"><span data-stu-id="2ffc0-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffc0-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ffc0-136">Header</span></span><br/> | <dl> <span data-ttu-id="2ffc0-137"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ffc0-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2ffc0-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ffc0-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="2ffc0-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ffc0-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ffc0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ffc0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffc0-141">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="2ffc0-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="2ffc0-142">**PST \_ ACCESSRULESET**</span><span class="sxs-lookup"><span data-stu-id="2ffc0-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="2ffc0-143">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="2ffc0-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
