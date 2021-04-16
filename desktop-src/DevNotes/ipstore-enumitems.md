---
description: Devuelve el puntero de interfaz de un subtipo para enumerar los elementos de la base de datos de almacenamiento protegido.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'IPStore:: EnumItems (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649662"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="22c31-103">IPStore:: EnumItems (método)</span><span class="sxs-lookup"><span data-stu-id="22c31-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="22c31-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22c31-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="22c31-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="22c31-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="22c31-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="22c31-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="22c31-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="22c31-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="22c31-108">Devuelve el puntero de interfaz de un subtipo para enumerar los elementos de la base de datos de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="22c31-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c31-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22c31-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="22c31-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22c31-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c31-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="22c31-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c31-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="22c31-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="22c31-113">Value</span><span class="sxs-lookup"><span data-stu-id="22c31-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="22c31-114">Significado</span><span class="sxs-lookup"><span data-stu-id="22c31-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="22c31-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="22c31-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="22c31-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="22c31-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="22c31-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="22c31-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="22c31-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="22c31-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22c31-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22c31-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c31-120">Un puntero a un **GUID** que identifica el tipo de datos del elemento que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="22c31-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="22c31-121">*pItemSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22c31-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c31-122">Un puntero a un **GUID** que identifica el subtipo de datos del elemento que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="22c31-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="22c31-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22c31-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c31-124">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="22c31-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="22c31-125">*ppenum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22c31-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c31-126">Un puntero a un puntero a una interfaz [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="22c31-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c31-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22c31-127">Return value</span></span>

<span data-ttu-id="22c31-128">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22c31-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="22c31-129">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="22c31-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c31-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c31-130">Requirements</span></span>



| <span data-ttu-id="22c31-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c31-131">Requirement</span></span> | <span data-ttu-id="22c31-132">Value</span><span class="sxs-lookup"><span data-stu-id="22c31-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c31-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22c31-133">Header</span></span><br/> | <dl> <span data-ttu-id="22c31-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c31-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="22c31-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22c31-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="22c31-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c31-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c31-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="22c31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c31-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="22c31-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
