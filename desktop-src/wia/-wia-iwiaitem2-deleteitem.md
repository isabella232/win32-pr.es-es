---
description: Quita el objeto IWiaItem2 actual del árbol de objetos del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2::D método eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715196"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="45939-103">IWiaItem2::D método eleteItem</span><span class="sxs-lookup"><span data-stu-id="45939-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="45939-104">Quita el objeto [**IWiaItem2**](-wia-iwiaitem2.md) actual del árbol de objetos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45939-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="45939-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45939-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="45939-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45939-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45939-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45939-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45939-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="45939-108">Type: **LONG**</span></span>

<span data-ttu-id="45939-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="45939-109">Currently unused.</span></span> <span data-ttu-id="45939-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="45939-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45939-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45939-111">Return value</span></span>

<span data-ttu-id="45939-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45939-112">Type: **HRESULT**</span></span>

<span data-ttu-id="45939-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="45939-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45939-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45939-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45939-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45939-115">Remarks</span></span>

<span data-ttu-id="45939-116">El sistema en tiempo de ejecución de adquisición de imágenes de Windows (WIA) 2,0 representa cada dispositivo de hardware WIA 2,0 conectado al equipo del usuario como un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="45939-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="45939-117">Un determinado dispositivo WIA 2,0 puede permitir o no que las aplicaciones eliminen objetos **IWiaItem2** de su árbol.</span><span class="sxs-lookup"><span data-stu-id="45939-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="45939-118">Los elementos que tienen elementos secundarios no se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="45939-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="45939-119">La interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) debe usarse para consultar el dispositivo para la capacidad de eliminación de elementos.</span><span class="sxs-lookup"><span data-stu-id="45939-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="45939-120">Si el dispositivo admite la eliminación de elementos en su árbol [**IWiaItem2**](-wia-iwiaitem2.md) , llame al método **IWiaItem2::D eleteitem** para quitar el objeto **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="45939-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="45939-121">Tenga en cuenta que este método solo elimina un objeto una vez que se han liberado todas las referencias al objeto.</span><span class="sxs-lookup"><span data-stu-id="45939-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="45939-122">Si se produce un error en la eliminación de un elemento, \_ se devuelve E DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="45939-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="45939-123">El valor numérico de este error aún no se ha definido.</span><span class="sxs-lookup"><span data-stu-id="45939-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="45939-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45939-124">Requirements</span></span>



| <span data-ttu-id="45939-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45939-125">Requirement</span></span> | <span data-ttu-id="45939-126">Value</span><span class="sxs-lookup"><span data-stu-id="45939-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45939-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45939-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45939-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45939-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45939-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45939-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45939-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45939-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="45939-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45939-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="45939-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="45939-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="45939-133">IDL</span><span class="sxs-lookup"><span data-stu-id="45939-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45939-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45939-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




