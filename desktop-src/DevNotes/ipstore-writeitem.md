---
description: Escribe un elemento de datos en el almacenamiento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore:: WriteItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650038"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="cc666-103">IPStore:: WriteItem (método)</span><span class="sxs-lookup"><span data-stu-id="cc666-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="cc666-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc666-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="cc666-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cc666-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="cc666-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="cc666-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="cc666-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="cc666-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="cc666-108">Escribe un elemento de datos en el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="cc666-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc666-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc666-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cc666-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc666-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc666-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-112">Área de almacenamiento del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cc666-112">The provider storage area.</span></span>



| <span data-ttu-id="cc666-113">Value</span><span class="sxs-lookup"><span data-stu-id="cc666-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="cc666-114">Significado</span><span class="sxs-lookup"><span data-stu-id="cc666-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="cc666-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="cc666-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="cc666-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="cc666-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="cc666-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="cc666-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cc666-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-120">Un puntero a un **GUID** que identifica el tipo de datos del elemento de datos que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="cc666-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-121">*pItemSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-122">Un puntero a un **GUID** que identifica el subtipo de datos del elemento de datos que se está escribiendo.</span><span class="sxs-lookup"><span data-stu-id="cc666-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-123">*szItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-124">Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.</span><span class="sxs-lookup"><span data-stu-id="cc666-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-125">*cbData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cc666-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-126">Un puntero a un **valor DWORD** que indica el tamaño del búfer que contiene el elemento de datos almacenado.</span><span class="sxs-lookup"><span data-stu-id="cc666-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-127">*ppbData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cc666-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-128">Puntero a un búfer que contiene el elemento de datos que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="cc666-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-129">*pProomptInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-130">Puntero a una [**estructura \_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cc666-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc666-131">*dwDefaultConfirmationStyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-132">El estilo de confirmación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cc666-132">The default confirmation style.</span></span>



| <span data-ttu-id="cc666-133">Value</span><span class="sxs-lookup"><span data-stu-id="cc666-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="cc666-134">Significado</span><span class="sxs-lookup"><span data-stu-id="cc666-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="cc666-135"><dt>**Archivo pst \_ CF \_ default**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="cc666-136">Permite al usuario elegir el estilo de confirmación.</span><span class="sxs-lookup"><span data-stu-id="cc666-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="cc666-137"><dt>**Archivo pst \_ CF \_ ninguno**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="cc666-138">Fuerza la creación del elemento silencioso.</span><span class="sxs-lookup"><span data-stu-id="cc666-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="cc666-139">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc666-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc666-140">La interfaz de usuario y los comportamientos de seguridad para la operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="cc666-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="cc666-141">Value</span><span class="sxs-lookup"><span data-stu-id="cc666-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="cc666-142">Significado</span><span class="sxs-lookup"><span data-stu-id="cc666-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="cc666-143"><dt>**Archivo pst \_ NO \_ sobrescribir**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="cc666-144">Especifica que el elemento se creará en el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="cc666-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="cc666-145">No se permite la sobrescritura de un elemento existente.</span><span class="sxs-lookup"><span data-stu-id="cc666-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="cc666-146"><dt>**Archivo pst \_ No RESTRINGIdo de \_ ITEMDATA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="cc666-147">Especifica que el flujo de datos no es seguro.</span><span class="sxs-lookup"><span data-stu-id="cc666-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="cc666-148">De forma predeterminada, las llamadas a elementos son seguras.</span><span class="sxs-lookup"><span data-stu-id="cc666-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc666-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc666-149">Return value</span></span>

<span data-ttu-id="cc666-150">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc666-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="cc666-151">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc666-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc666-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc666-152">Requirements</span></span>



| <span data-ttu-id="cc666-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc666-153">Requirement</span></span> | <span data-ttu-id="cc666-154">Value</span><span class="sxs-lookup"><span data-stu-id="cc666-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc666-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc666-155">Header</span></span><br/> | <dl> <span data-ttu-id="cc666-156"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="cc666-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc666-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="cc666-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc666-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc666-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc666-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc666-160">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="cc666-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="cc666-161">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="cc666-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
