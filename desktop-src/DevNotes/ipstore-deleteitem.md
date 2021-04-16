---
description: Elimina el elemento especificado del almacenamiento protegido.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: IPStore::D método eleteItem (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650020"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="da333-103">IPStore::D método eleteItem</span><span class="sxs-lookup"><span data-stu-id="da333-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="da333-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da333-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="da333-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="da333-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="da333-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="da333-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="da333-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="da333-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="da333-108">Elimina el elemento especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="da333-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="da333-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da333-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="da333-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da333-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da333-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="da333-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-112">Área de almacenamiento del proveedor.</span><span class="sxs-lookup"><span data-stu-id="da333-112">The provider storage area.</span></span>



| <span data-ttu-id="da333-113">Value</span><span class="sxs-lookup"><span data-stu-id="da333-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="da333-114">Significado</span><span class="sxs-lookup"><span data-stu-id="da333-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="da333-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="da333-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="da333-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="da333-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="da333-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="da333-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="da333-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="da333-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="da333-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da333-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-120">Un puntero a un **GUID** que identifica el tipo de datos del elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="da333-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="da333-121">*pItemSubType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da333-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-122">**GUID** que indica el subtipo de elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="da333-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="da333-123">*szItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da333-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-124">Cadena que contiene el nombre del elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="da333-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="da333-125">*pPromptInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da333-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-126">Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="da333-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da333-127">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da333-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da333-128">Especifica la interfaz de usuario y los comportamientos de seguridad para la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="da333-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="da333-129">Value</span><span class="sxs-lookup"><span data-stu-id="da333-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="da333-130">Significado</span><span class="sxs-lookup"><span data-stu-id="da333-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="da333-131"><dt>**Archivo pst \_ SIN \_ \_ migración de IU**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="da333-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="da333-132">No mostrar la interfaz de usuario a menos que se requiera una contraseña personalizada.</span><span class="sxs-lookup"><span data-stu-id="da333-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da333-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da333-133">Return value</span></span>

<span data-ttu-id="da333-134">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da333-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="da333-135">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="da333-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="da333-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da333-136">Requirements</span></span>



| <span data-ttu-id="da333-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="da333-137">Requirement</span></span> | <span data-ttu-id="da333-138">Value</span><span class="sxs-lookup"><span data-stu-id="da333-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da333-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da333-139">Header</span></span><br/> | <dl> <span data-ttu-id="da333-140"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="da333-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="da333-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da333-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="da333-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da333-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da333-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="da333-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da333-144">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="da333-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="da333-145">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="da333-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
