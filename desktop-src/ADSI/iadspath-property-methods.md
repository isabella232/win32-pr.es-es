---
title: Métodos de la propiedad IADsPath (iAds. h)
description: El método Property de la interfaz IADsPath establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPath ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803163"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="5c7ee-105">Métodos de propiedad IADsPath</span><span class="sxs-lookup"><span data-stu-id="5c7ee-105">IADsPath Property Methods</span></span>

<span data-ttu-id="5c7ee-106">El método Property de la interfaz [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) establece la propiedad que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="5c7ee-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5c7ee-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5c7ee-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c7ee-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5c7ee-109">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-109">**Path**</span></span>
<span data-ttu-id="5c7ee-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5c7ee-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5c7ee-111">Ruta de acceso de un directorio del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="5c7ee-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5c7ee-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c7ee-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c7ee-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-114">**Type**</span></span>
<span data-ttu-id="5c7ee-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5c7ee-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5c7ee-116">Tipo de archivo del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="5c7ee-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5c7ee-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c7ee-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c7ee-119">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-119">**VolumeName**</span></span>
<span data-ttu-id="5c7ee-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5c7ee-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="5c7ee-121">Nombre de un volumen existente del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="5c7ee-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5c7ee-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c7ee-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="5c7ee-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7ee-124">Requirements</span></span>



| <span data-ttu-id="5c7ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7ee-125">Requirement</span></span> | <span data-ttu-id="5c7ee-126">Value</span><span class="sxs-lookup"><span data-stu-id="5c7ee-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ee-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c7ee-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7ee-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c7ee-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c7ee-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c7ee-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7ee-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c7ee-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c7ee-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c7ee-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7ee-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7ee-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5c7ee-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c7ee-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c7ee-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c7ee-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c7ee-135">IID</span><span class="sxs-lookup"><span data-stu-id="5c7ee-135">IID</span></span><br/>                      | <span data-ttu-id="5c7ee-136">IID \_ IADsPath se define como B287FCD5-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="5c7ee-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5c7ee-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c7ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7ee-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="5c7ee-139">**Ruta de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





