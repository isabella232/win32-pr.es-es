---
description: Abre un elemento para varios accesos.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore:: OpenItem (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670357"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="c4a93-103">IPStore:: OpenItem (método)</span><span class="sxs-lookup"><span data-stu-id="c4a93-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="c4a93-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c4a93-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c4a93-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c4a93-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c4a93-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="c4a93-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c4a93-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c4a93-108">Abre un elemento para varios accesos.</span><span class="sxs-lookup"><span data-stu-id="c4a93-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a93-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4a93-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c4a93-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4a93-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a93-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="c4a93-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="c4a93-113">Value</span><span class="sxs-lookup"><span data-stu-id="c4a93-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="c4a93-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c4a93-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="c4a93-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="c4a93-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="c4a93-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="c4a93-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c4a93-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="c4a93-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c4a93-119">*pItemType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-120">Un puntero a un GUID que identifica el tipo de datos del elemento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="c4a93-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="c4a93-121">*pItemSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-122">Un puntero a un GUID que indica el subtipo de elemento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="c4a93-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="c4a93-123">*szItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-124">Cadena que contiene el nombre del elemento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="c4a93-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="c4a93-125">*ModeFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-126">Describe los modos de acceso a los que pertenece un conjunto especificado de cláusulas de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4a93-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="c4a93-127">Para obtener más información, vea [**PStore Types**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4a93-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="c4a93-128">Value</span><span class="sxs-lookup"><span data-stu-id="c4a93-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="c4a93-129">Significado</span><span class="sxs-lookup"><span data-stu-id="c4a93-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="c4a93-130"><dt>**Archivo pst \_ LEER**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="c4a93-131">Modo de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="c4a93-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="c4a93-132"><dt>**Archivo pst \_ ESCRIBIR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="c4a93-133">Modo de acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="c4a93-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c4a93-134">*pProomptInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-135">Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a93-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4a93-136">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4a93-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a93-137">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="c4a93-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a93-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4a93-138">Return value</span></span>

<span data-ttu-id="c4a93-139">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4a93-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="c4a93-140">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c4a93-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a93-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4a93-141">Remarks</span></span>

<span data-ttu-id="c4a93-142">El uso de **OpenItem** para abrir un elemento en la base de datos de almacenamiento protegido requiere que finalmente se cierre mediante [**IPStore:: CloseItem**](ipstore-closeitem.md) para evitar una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="c4a93-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a93-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a93-143">Requirements</span></span>



| <span data-ttu-id="c4a93-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a93-144">Requirement</span></span> | <span data-ttu-id="c4a93-145">Value</span><span class="sxs-lookup"><span data-stu-id="c4a93-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a93-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4a93-146">Header</span></span><br/> | <dl> <span data-ttu-id="c4a93-147"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c4a93-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4a93-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="c4a93-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4a93-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4a93-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4a93-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a93-151">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="c4a93-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="c4a93-152">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="c4a93-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
