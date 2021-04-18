---
description: El método GetCount recupera el número de elementos de la colección.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650167"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="fbeb0-103">IPortableDeviceValues:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="fbeb0-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="fbeb0-104">El método **getCount** recupera el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbeb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbeb0-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="fbeb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbeb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbeb0-107">*pcelt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbeb0-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeb0-108">Puntero a un **valor DWORD** que contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbeb0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbeb0-109">Return value</span></span>

<span data-ttu-id="fbeb0-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fbeb0-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fbeb0-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fbeb0-112">Return code</span></span>                                                                          | <span data-ttu-id="fbeb0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbeb0-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fbeb0-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fbeb0-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fbeb0-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="fbeb0-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fbeb0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbeb0-116">Requirements</span></span>



| <span data-ttu-id="fbeb0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbeb0-117">Requirement</span></span> | <span data-ttu-id="fbeb0-118">Value</span><span class="sxs-lookup"><span data-stu-id="fbeb0-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeb0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbeb0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fbeb0-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeb0-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbeb0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbeb0-121">Library</span></span><br/> | <dl> <span data-ttu-id="fbeb0-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbeb0-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbeb0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbeb0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbeb0-124">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="fbeb0-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




