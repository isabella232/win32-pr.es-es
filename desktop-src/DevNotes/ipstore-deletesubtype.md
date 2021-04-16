---
description: Elimina un subtipo especificado en el tipo especificado.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: IPStore::D método eleteSubtype (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 6fd89c1dd00a71cb843596e08bc168b90008b180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650019"
---
# <a name="ipstoredeletesubtype-method"></a><span data-ttu-id="a4315-103">IPStore::D método eleteSubtype</span><span class="sxs-lookup"><span data-stu-id="a4315-103">IPStore::DeleteSubtype method</span></span>

<span data-ttu-id="a4315-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4315-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a4315-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a4315-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a4315-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="a4315-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a4315-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a4315-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a4315-108">Elimina un subtipo especificado en el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a4315-108">Deletes a specified subtype from within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4315-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4315-109">Syntax</span></span>


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a4315-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4315-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4315-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a4315-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4315-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="a4315-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="a4315-113">Value</span><span class="sxs-lookup"><span data-stu-id="a4315-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a4315-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a4315-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="a4315-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a4315-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="a4315-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="a4315-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="a4315-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a4315-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a4315-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="a4315-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a4315-119">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4315-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4315-120">Un puntero a un GUID que identifica el tipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a4315-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="a4315-121">*pSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4315-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4315-122">Un puntero a un GUID que identifica el subtipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a4315-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="a4315-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4315-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4315-124">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="a4315-124">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4315-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4315-125">Return value</span></span>

<span data-ttu-id="a4315-126">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4315-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="a4315-127">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4315-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4315-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4315-128">Requirements</span></span>



| <span data-ttu-id="a4315-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4315-129">Requirement</span></span> | <span data-ttu-id="a4315-130">Value</span><span class="sxs-lookup"><span data-stu-id="a4315-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4315-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4315-131">Header</span></span><br/> | <dl> <span data-ttu-id="a4315-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4315-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a4315-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4315-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="a4315-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4315-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4315-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4315-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4315-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="a4315-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
