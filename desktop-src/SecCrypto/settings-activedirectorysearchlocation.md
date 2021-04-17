---
description: Establece o recupera la ubicación de búsqueda de Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propiedad settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671094"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="ea85b-103">Propiedad settings. ActiveDirectorySearchLocation</span><span class="sxs-lookup"><span data-stu-id="ea85b-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="ea85b-104">\[La propiedad **ActiveDirectorySearchLocation** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="ea85b-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="ea85b-105">La propiedad **ActiveDirectorySearchLocation** establece o recupera la ubicación de búsqueda Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea85b-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea85b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea85b-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="ea85b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ea85b-107">Property value</span></span>

<span data-ttu-id="ea85b-108">Un valor de la enumeración de la [**\_ Ubicación de búsqueda de Active \_ Directory \_ \_ de CAPICOM**](capicom-active-directory-search-location.md) que especifica la ubicación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ea85b-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="ea85b-109">El valor predeterminado es CAPICOM \_ Search \_ any.</span><span class="sxs-lookup"><span data-stu-id="ea85b-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="ea85b-110">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ea85b-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="ea85b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ea85b-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="ea85b-112">Significado</span><span class="sxs-lookup"><span data-stu-id="ea85b-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="ea85b-113"><dt>**CAPICOM \_ Search \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="ea85b-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="ea85b-114">Buscar en todas las ubicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="ea85b-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="ea85b-115"><dt>**\_ \_ dominio predeterminado de búsqueda de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ea85b-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="ea85b-116">Buscar solo en el dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ea85b-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="ea85b-117"><dt>**CAPICOM \_ Buscar en el \_ \_ catálogo global**</dt></span><span class="sxs-lookup"><span data-stu-id="ea85b-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="ea85b-118">Buscar solo en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="ea85b-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea85b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea85b-119">Requirements</span></span>



| <span data-ttu-id="ea85b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea85b-120">Requirement</span></span> | <span data-ttu-id="ea85b-121">Value</span><span class="sxs-lookup"><span data-stu-id="ea85b-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea85b-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ea85b-122">Redistributable</span></span><br/> | <span data-ttu-id="ea85b-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea85b-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ea85b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea85b-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="ea85b-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea85b-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea85b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea85b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea85b-127">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="ea85b-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




