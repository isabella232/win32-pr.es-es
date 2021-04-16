---
description: Lee el elemento de datos especificado del almacenamiento protegido.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore:: ReadItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671466"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="87302-103">IPStore:: ReadItem (método)</span><span class="sxs-lookup"><span data-stu-id="87302-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="87302-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="87302-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="87302-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="87302-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="87302-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="87302-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="87302-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="87302-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="87302-108">Lee el elemento de datos especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="87302-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="87302-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87302-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="87302-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87302-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87302-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="87302-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-112">Área de almacenamiento del proveedor.</span><span class="sxs-lookup"><span data-stu-id="87302-112">The provider storage area.</span></span>



| <span data-ttu-id="87302-113">Value</span><span class="sxs-lookup"><span data-stu-id="87302-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="87302-114">Significado</span><span class="sxs-lookup"><span data-stu-id="87302-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="87302-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="87302-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="87302-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="87302-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="87302-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="87302-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="87302-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="87302-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="87302-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-120">Un puntero a un GUID que identifica el tipo de datos del elemento que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="87302-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="87302-121">*pItemSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-122">Un puntero a un GUID que identifica el subtipo de datos del elemento que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="87302-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="87302-123">*szItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-124">Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.</span><span class="sxs-lookup"><span data-stu-id="87302-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="87302-125">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-126">**DWORD** que indica el tamaño del búfer que contiene el elemento de datos almacenado.</span><span class="sxs-lookup"><span data-stu-id="87302-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="87302-127">*pbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-128">Puntero a un búfer que contiene el elemento de datos almacenado.</span><span class="sxs-lookup"><span data-stu-id="87302-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="87302-129">*pPromptInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-130">Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="87302-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87302-131">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87302-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87302-132">Especifica la interfaz de usuario y los comportamientos de seguridad para la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="87302-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="87302-133">Los valores de marca se pueden combinar con un operador lógico OR.</span><span class="sxs-lookup"><span data-stu-id="87302-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="87302-134">Value</span><span class="sxs-lookup"><span data-stu-id="87302-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="87302-135">Significado</span><span class="sxs-lookup"><span data-stu-id="87302-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="87302-136"><dt>**Archivo pst \_ No RESTRINGIdo de \_ ITEMDATA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="87302-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="87302-137">Especifica que el flujo de datos no es seguro.</span><span class="sxs-lookup"><span data-stu-id="87302-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="87302-138">De forma predeterminada, las llamadas a elementos son seguras.</span><span class="sxs-lookup"><span data-stu-id="87302-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="87302-139"><dt>**Archivo pst \_ SOLICITAR \_ consulta**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="87302-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="87302-140">Especifica que la confirmación se devolverá cuando se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="87302-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="87302-141">Si la interfaz de usuario está habilitada, se devuelve una operación correcta de **PST \_ E \_ Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="87302-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="87302-142">Si la interfaz de usuario no está habilitada, se devuelve un valor de **\_ \_ elemento \_ PST E** .</span><span class="sxs-lookup"><span data-stu-id="87302-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="87302-143"><dt>**Archivo pst \_ SIN \_ \_ migración de IU**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="87302-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="87302-144">No mostrar la interfaz de usuario a menos que se requiera una contraseña personalizada.</span><span class="sxs-lookup"><span data-stu-id="87302-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87302-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87302-145">Return value</span></span>

<span data-ttu-id="87302-146">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87302-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="87302-147">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="87302-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="87302-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87302-148">Remarks</span></span>

<span data-ttu-id="87302-149">Si **ReadItem** se completa correctamente, la aplicación es responsable de liberar el búfer de datos devuelto mediante la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="87302-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="87302-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87302-150">Requirements</span></span>



| <span data-ttu-id="87302-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="87302-151">Requirement</span></span> | <span data-ttu-id="87302-152">Value</span><span class="sxs-lookup"><span data-stu-id="87302-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87302-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87302-153">Header</span></span><br/> | <dl> <span data-ttu-id="87302-154"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="87302-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="87302-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87302-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="87302-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87302-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87302-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="87302-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87302-158">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="87302-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="87302-159">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="87302-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
