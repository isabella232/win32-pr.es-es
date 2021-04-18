---
title: WMDRM_LICENSE_FILTER estructura (wmdrmsdk. h)
description: La \_ estructura del \_ filtro de licencias de WMDRM define los parámetros de filtrado para su uso al crear una enumeración de licencias.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699526"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="017eb-105">Estructura del filtro de \_ licencias de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="017eb-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="017eb-106">La estructura del **\_ \_ filtro de licencias de WMDRM** define los parámetros de filtrado para su uso al crear una enumeración de licencias.</span><span class="sxs-lookup"><span data-stu-id="017eb-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="017eb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="017eb-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="017eb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="017eb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="017eb-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="017eb-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="017eb-110">Especifica un número de versión mínimo para las licencias devueltas.</span><span class="sxs-lookup"><span data-stu-id="017eb-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-111">**bstrKID**</span><span class="sxs-lookup"><span data-stu-id="017eb-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="017eb-112">Especifica un identificador de clave para el que filtrar licencias.</span><span class="sxs-lookup"><span data-stu-id="017eb-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="017eb-113">Solo se incluirán en la enumeración las licencias con el identificador de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="017eb-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-114">**bstrRights**</span><span class="sxs-lookup"><span data-stu-id="017eb-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="017eb-115">Especifica un conjunto de derechos para filtrar licencias.</span><span class="sxs-lookup"><span data-stu-id="017eb-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="017eb-116">En la enumeración solo se incluirán las licencias que proporcionen todos los derechos especificados.</span><span class="sxs-lookup"><span data-stu-id="017eb-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-117">**bstrAllowedSourceIDs**</span><span class="sxs-lookup"><span data-stu-id="017eb-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="017eb-118">Especifica los orígenes de contenido protegido que se incluirán en la búsqueda de licencias.</span><span class="sxs-lookup"><span data-stu-id="017eb-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="017eb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="017eb-119">Remarks</span></span>

<span data-ttu-id="017eb-120">El método [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="017eb-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="017eb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="017eb-121">Requirements</span></span>



| <span data-ttu-id="017eb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="017eb-122">Requirement</span></span> | <span data-ttu-id="017eb-123">Value</span><span class="sxs-lookup"><span data-stu-id="017eb-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="017eb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="017eb-124">Header</span></span><br/> | <dl> <span data-ttu-id="017eb-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="017eb-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017eb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="017eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017eb-127">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="017eb-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





