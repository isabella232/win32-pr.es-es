---
description: Define las formas de asignación a un identificador de clase.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumeración TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649501"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="6e659-103">Enumeración TYSPEC</span><span class="sxs-lookup"><span data-stu-id="6e659-103">TYSPEC enumeration</span></span>

<span data-ttu-id="6e659-104">Define las formas de asignación a un identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="6e659-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e659-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e659-105">Syntax</span></span>


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a><span data-ttu-id="6e659-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6e659-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6e659-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6e659-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-108">UN CLSID.</span><span class="sxs-lookup"><span data-stu-id="6e659-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**</span><span class="sxs-lookup"><span data-stu-id="6e659-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-110">Extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6e659-110">A file name extension.</span></span> <span data-ttu-id="6e659-111">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ Mimetype**</span><span class="sxs-lookup"><span data-stu-id="6e659-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-113">Tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="6e659-113">A MIME type.</span></span> <span data-ttu-id="6e659-114">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nombre de archivo TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="6e659-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-116">Un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6e659-116">A file name.</span></span> <span data-ttu-id="6e659-117">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="6e659-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-119">UN PROGID.</span><span class="sxs-lookup"><span data-stu-id="6e659-119">A PROGID.</span></span> <span data-ttu-id="6e659-120">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PACKAGENAME**</span><span class="sxs-lookup"><span data-stu-id="6e659-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-122">Un nombre de paquete.</span><span class="sxs-lookup"><span data-stu-id="6e659-122">A package name.</span></span> <span data-ttu-id="6e659-123">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e659-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC \_ objectId**</span><span class="sxs-lookup"><span data-stu-id="6e659-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="6e659-125">IDENTIFICADOR de objeto.</span><span class="sxs-lookup"><span data-stu-id="6e659-125">An object ID.</span></span> <span data-ttu-id="6e659-126">Este valor no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e659-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e659-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e659-127">Remarks</span></span>

<span data-ttu-id="6e659-128">La Unión **uCLSSPEC** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6e659-128">The **uCLSSPEC** union is defined as follows:</span></span>

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a><span data-ttu-id="6e659-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e659-129">Requirements</span></span>



| <span data-ttu-id="6e659-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e659-130">Requirement</span></span> | <span data-ttu-id="6e659-131">Value</span><span class="sxs-lookup"><span data-stu-id="6e659-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e659-132">IDL</span><span class="sxs-lookup"><span data-stu-id="6e659-132">IDL</span></span><br/> | <dl> <span data-ttu-id="6e659-133"><dt>Wtypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e659-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e659-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e659-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e659-135">**Coinstalación**</span><span class="sxs-lookup"><span data-stu-id="6e659-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
