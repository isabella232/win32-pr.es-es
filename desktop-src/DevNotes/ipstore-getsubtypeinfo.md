---
description: Recupera información asociada a un subtipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'IPStore:: GetSubtypeInfo (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671348"
---
# <a name="ipstoregetsubtypeinfo-method"></a><span data-ttu-id="016e8-103">IPStore:: GetSubtypeInfo (método)</span><span class="sxs-lookup"><span data-stu-id="016e8-103">IPStore::GetSubtypeInfo method</span></span>

<span data-ttu-id="016e8-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="016e8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="016e8-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="016e8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="016e8-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="016e8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="016e8-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="016e8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="016e8-108">Recupera información asociada a un subtipo.</span><span class="sxs-lookup"><span data-stu-id="016e8-108">Retrieves information associated with a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="016e8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="016e8-109">Syntax</span></span>


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="016e8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="016e8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="016e8-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="016e8-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016e8-112">Área de almacenamiento del proveedor.</span><span class="sxs-lookup"><span data-stu-id="016e8-112">The provider storage area.</span></span>



| <span data-ttu-id="016e8-113">Value</span><span class="sxs-lookup"><span data-stu-id="016e8-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="016e8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="016e8-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="016e8-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="016e8-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="016e8-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="016e8-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="016e8-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="016e8-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="016e8-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="016e8-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="016e8-119">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="016e8-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016e8-120">Un puntero a un GUID que identifica el tipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="016e8-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="016e8-121">*pSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="016e8-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016e8-122">Un puntero a un GUID que identifica el subtipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="016e8-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="016e8-123">*ppInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="016e8-123">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016e8-124">Puntero a una estructura [**de \_ TYPEINFO de PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="016e8-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="016e8-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="016e8-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016e8-126">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="016e8-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="016e8-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="016e8-127">Return value</span></span>

<span data-ttu-id="016e8-128">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="016e8-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="016e8-129">Un valor de PST \_ E \_ OK indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="016e8-129">A value of PST\_E\_OK indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="016e8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="016e8-130">Requirements</span></span>



| <span data-ttu-id="016e8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="016e8-131">Requirement</span></span> | <span data-ttu-id="016e8-132">Value</span><span class="sxs-lookup"><span data-stu-id="016e8-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="016e8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="016e8-133">Header</span></span><br/> | <dl> <span data-ttu-id="016e8-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="016e8-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="016e8-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="016e8-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="016e8-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016e8-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016e8-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="016e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016e8-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="016e8-138">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="016e8-139">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="016e8-139">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
