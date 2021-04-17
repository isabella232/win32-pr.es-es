---
title: Enumeración WMDM_STORAGE_ENUM_MODE
description: El \_ tipo de \_ enumeración de modo de enumeración de almacenamiento WMDM \_ define cómo se va a enumerar el contenido del almacenamiento. IWMDMStorage3 SetEnumPreference usa esta enumeración.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Enumeración WMDM_STORAGE_ENUM_MODE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698642"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="ac4b1-105">\_ \_ Enumeración de modo de enumeración de almacenamiento WMDM \_</span><span class="sxs-lookup"><span data-stu-id="ac4b1-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="ac4b1-106">El tipo de enumeración de **\_ \_ \_ modo de enumeración de almacenamiento WMDM** define cómo se va a enumerar el contenido del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="ac4b1-107">[**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)usa esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac4b1-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="ac4b1-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ac4b1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ac4b1-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modo de ENUMERAción \_ \_ sin formato**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="ac4b1-111">Enumera el contenido del almacenamiento tal como está organizado en el sistema de archivos del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="ac4b1-112">**modo de ENUMERAción \_ \_ use \_ Pref de dispositivo \_**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="ac4b1-113">Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="ac4b1-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="ac4b1-114">**\_vistas de \_ metadatos de modo de enumeración \_**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="ac4b1-115">Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="ac4b1-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**modo de ENUMERAción \_ \_ use \_ Pref de dispositivo \_**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="ac4b1-117">Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="ac4b1-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="ac4b1-118">**\_vistas de \_ metadatos de modo de enumeración \_**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="ac4b1-119">Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="ac4b1-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_vistas de \_ metadatos de modo de enumeración \_**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="ac4b1-121">Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ac4b1-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac4b1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac4b1-122">Requirements</span></span>



| <span data-ttu-id="ac4b1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac4b1-123">Requirement</span></span> | <span data-ttu-id="ac4b1-124">Value</span><span class="sxs-lookup"><span data-stu-id="ac4b1-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4b1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac4b1-125">Header</span></span><br/> | <dl> <span data-ttu-id="ac4b1-126"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac4b1-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4b1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac4b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4b1-128">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="ac4b1-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





