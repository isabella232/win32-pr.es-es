---
title: Tipos de modificación de atributos ADSI (iAds. h)
description: Se usa con el miembro dwControlCode de la estructura de información de atributos de ADS \_ \_ para especificar el tipo de operación que se va a realizar cuando se modifica un atributo con el método SetObjectAttributes de IDirectoryObject.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- tipos de modificación de atributos ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079084"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="022eb-104">Tipos de modificación de atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="022eb-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="022eb-105">Las constantes siguientes se usan con el miembro **dwControlCode** de la estructura [**ADS \_ ATTR \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para especificar el tipo de operación que se va a realizar cuando se modifica un atributo con el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="022eb-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="022eb-106">Para obtener más información sobre el uso de estos valores, vea [modificar atributos con ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="022eb-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="022eb-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_claridad del atributo ADS \_**</span><span class="sxs-lookup"><span data-stu-id="022eb-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022eb-108">1</span><span class="sxs-lookup"><span data-stu-id="022eb-108">1</span></span>
</dt> <dt>



<span data-ttu-id="022eb-109">Hace que se quiten todos los valores de atributo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="022eb-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="022eb-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_actualización de atributos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="022eb-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022eb-111">2</span><span class="sxs-lookup"><span data-stu-id="022eb-111">2</span></span>
</dt> <dt>



<span data-ttu-id="022eb-112">Hace que se actualicen los valores de atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="022eb-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="022eb-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS \_ ATTR \_ Append**</span><span class="sxs-lookup"><span data-stu-id="022eb-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022eb-114">3</span><span class="sxs-lookup"><span data-stu-id="022eb-114">3</span></span>
</dt> <dt>



<span data-ttu-id="022eb-115">Hace que los valores de atributo especificados se anexen a los valores de atributo existentes.</span><span class="sxs-lookup"><span data-stu-id="022eb-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="022eb-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS \_ ATTR \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="022eb-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022eb-117">4</span><span class="sxs-lookup"><span data-stu-id="022eb-117">4</span></span>
</dt> <dt>



<span data-ttu-id="022eb-118">Hace que los valores de atributo especificados se quiten de un objeto.</span><span class="sxs-lookup"><span data-stu-id="022eb-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="022eb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="022eb-119">Remarks</span></span>

<span data-ttu-id="022eb-120">Estas constantes están diseñadas para usarse con la estructura [**de \_ \_ información de atributos de ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) en el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="022eb-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="022eb-121">Estas constantes no se deben confundir con miembros de la enumeración de la enumeración de la [**\_ operación de propiedad \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , que están diseñadas para usarse con el método [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="022eb-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="022eb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="022eb-122">Requirements</span></span>



| <span data-ttu-id="022eb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="022eb-123">Requirement</span></span> | <span data-ttu-id="022eb-124">Value</span><span class="sxs-lookup"><span data-stu-id="022eb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="022eb-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="022eb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="022eb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="022eb-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="022eb-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="022eb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="022eb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="022eb-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="022eb-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="022eb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="022eb-130"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="022eb-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022eb-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="022eb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022eb-132">**\_información de atributos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="022eb-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="022eb-133">**IDirectoryObject::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="022eb-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="022eb-134">Modificar atributos con ADSI</span><span class="sxs-lookup"><span data-stu-id="022eb-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





