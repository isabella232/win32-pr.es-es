---
description: Cierra un elemento de datos especificado de un almacenamiento protegido.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'IPStore:: CloseItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670813"
---
# <a name="ipstorecloseitem-method"></a><span data-ttu-id="ba053-103">IPStore:: CloseItem (método)</span><span class="sxs-lookup"><span data-stu-id="ba053-103">IPStore::CloseItem method</span></span>

<span data-ttu-id="ba053-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba053-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ba053-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ba053-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ba053-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="ba053-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ba053-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ba053-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ba053-108">Cierra un elemento de datos especificado de un almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="ba053-108">Closes a specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba053-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba053-109">Syntax</span></span>


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ba053-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba053-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba053-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ba053-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba053-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="ba053-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="ba053-113">Value</span><span class="sxs-lookup"><span data-stu-id="ba053-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ba053-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ba053-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="ba053-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="ba053-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="ba053-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="ba053-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="ba053-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ba053-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ba053-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="ba053-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba053-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba053-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba053-120">Un puntero a un **GUID** que identifica el tipo de datos del elemento que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="ba053-120">A pointer to a **GUID** that identifies the data type of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="ba053-121">*pItemSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba053-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba053-122">Un puntero a un **GUID** que indica el subtipo de elemento que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="ba053-122">A pointer to a **GUID** that indicates the item subtype to close.</span></span>

</dd> <dt>

<span data-ttu-id="ba053-123">*szItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba053-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba053-124">Cadena que contiene el nombre del elemento que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="ba053-124">A string that contains the name of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="ba053-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba053-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba053-126">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="ba053-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba053-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba053-127">Return value</span></span>

<span data-ttu-id="ba053-128">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba053-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="ba053-129">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba053-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba053-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba053-130">Requirements</span></span>



| <span data-ttu-id="ba053-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba053-131">Requirement</span></span> | <span data-ttu-id="ba053-132">Value</span><span class="sxs-lookup"><span data-stu-id="ba053-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba053-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba053-133">Header</span></span><br/> | <dl> <span data-ttu-id="ba053-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba053-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ba053-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba053-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="ba053-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba053-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba053-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba053-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba053-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ba053-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
