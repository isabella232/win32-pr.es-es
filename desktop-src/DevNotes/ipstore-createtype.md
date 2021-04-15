---
description: Crea el tipo especificado con el nombre especificado.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'IPStore:: CreateType (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7a8c855fd5b50adf41986ef27a1bd296894b12bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649505"
---
# <a name="ipstorecreatetype-method"></a><span data-ttu-id="8f3f8-103">IPStore:: CreateType (método)</span><span class="sxs-lookup"><span data-stu-id="8f3f8-103">IPStore::CreateType method</span></span>

<span data-ttu-id="8f3f8-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="8f3f8-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="8f3f8-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="8f3f8-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="8f3f8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="8f3f8-108">Crea el tipo especificado con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-108">Creates the specified type with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3f8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f3f8-109">Syntax</span></span>


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8f3f8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f3f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3f8-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8f3f8-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f8-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="8f3f8-113">Value</span><span class="sxs-lookup"><span data-stu-id="8f3f8-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="8f3f8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8f3f8-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="8f3f8-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="8f3f8-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="8f3f8-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="8f3f8-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8f3f8-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="8f3f8-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f3f8-119">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f3f8-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f8-120">Un puntero a un **GUID** que identifica el tipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="8f3f8-121">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f3f8-121">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f8-122">Puntero a una estructura [**de \_ TYPEINFO de PST**](pst-typeinfo.md) que contiene el nombre del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="8f3f8-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f3f8-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f8-124">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3f8-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f3f8-125">Return value</span></span>

<span data-ttu-id="8f3f8-126">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f3f8-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="8f3f8-127">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f3f8-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3f8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3f8-128">Requirements</span></span>



| <span data-ttu-id="8f3f8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3f8-129">Requirement</span></span> | <span data-ttu-id="8f3f8-130">Value</span><span class="sxs-lookup"><span data-stu-id="8f3f8-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3f8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f3f8-131">Header</span></span><br/> | <dl> <span data-ttu-id="8f3f8-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3f8-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="8f3f8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f3f8-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="8f3f8-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3f8-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f3f8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f3f8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3f8-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="8f3f8-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="8f3f8-137">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="8f3f8-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
