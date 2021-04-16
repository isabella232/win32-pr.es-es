---
description: Recupera información asociada a un tipo.
ms.assetid: 27a283a5-8924-4a2f-8f58-e673a424e28a
title: 'IPStore:: GetTypeInfo (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetTypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: c533c30268bf8b8e879e937359471da8cd7af8b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649983"
---
# <a name="ipstoregettypeinfo-method"></a><span data-ttu-id="0abfb-103">IPStore:: GetTypeInfo (método)</span><span class="sxs-lookup"><span data-stu-id="0abfb-103">IPStore::GetTypeInfo method</span></span>

<span data-ttu-id="0abfb-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0abfb-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0abfb-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0abfb-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0abfb-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="0abfb-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0abfb-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0abfb-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0abfb-108">Recupera información asociada a un tipo.</span><span class="sxs-lookup"><span data-stu-id="0abfb-108">Retrieves information associated with a type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abfb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0abfb-109">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0abfb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0abfb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abfb-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0abfb-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abfb-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="0abfb-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="0abfb-113">Value</span><span class="sxs-lookup"><span data-stu-id="0abfb-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0abfb-114">Significado</span><span class="sxs-lookup"><span data-stu-id="0abfb-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="0abfb-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0abfb-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="0abfb-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="0abfb-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="0abfb-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0abfb-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0abfb-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="0abfb-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0abfb-119">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0abfb-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abfb-120">Un puntero a un **GUID** que identifica el tipo de datos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0abfb-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="0abfb-121">*ppInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0abfb-121">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abfb-122">Puntero a una estructura [**de \_ TYPEINFO de PST**](pst-typeinfo.md) que contiene el nombre del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0abfb-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="0abfb-123">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0abfb-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abfb-124">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="0abfb-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abfb-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0abfb-125">Return value</span></span>

<span data-ttu-id="0abfb-126">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0abfb-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="0abfb-127">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0abfb-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abfb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0abfb-128">Requirements</span></span>



| <span data-ttu-id="0abfb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abfb-129">Requirement</span></span> | <span data-ttu-id="0abfb-130">Value</span><span class="sxs-lookup"><span data-stu-id="0abfb-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0abfb-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0abfb-131">Header</span></span><br/> | <dl> <span data-ttu-id="0abfb-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0abfb-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0abfb-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0abfb-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="0abfb-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0abfb-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abfb-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0abfb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abfb-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="0abfb-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="0abfb-137">**TYPEINFO de PST \_**</span><span class="sxs-lookup"><span data-stu-id="0abfb-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
