---
description: 'Método IPortableDeviceValuesCollection::GetCount: el método GetCount recupera el número de elementos de la colección.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: Método IPortableDeviceValuesCollection::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083183"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="aadbb-103">IPortableDeviceValuesCollection::GetCount (Método)</span><span class="sxs-lookup"><span data-stu-id="aadbb-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="aadbb-104">El **método GetCount** recupera el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="aadbb-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aadbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aadbb-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="aadbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aadbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aadbb-107">*pcElems* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aadbb-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aadbb-108">Puntero a un **DWORD** que contiene el número de **interfaces IPortableDeviceValues** de la colección.</span><span class="sxs-lookup"><span data-stu-id="aadbb-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aadbb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aadbb-109">Return value</span></span>

<span data-ttu-id="aadbb-110">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="aadbb-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aadbb-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="aadbb-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aadbb-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aadbb-112">Return code</span></span>                                                                               | <span data-ttu-id="aadbb-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="aadbb-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="aadbb-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aadbb-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="aadbb-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="aadbb-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="aadbb-116"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="aadbb-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="aadbb-117">Un argumento de puntero necesario era **NULL.**</span><span class="sxs-lookup"><span data-stu-id="aadbb-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aadbb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aadbb-118">Requirements</span></span>



| <span data-ttu-id="aadbb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aadbb-119">Requirement</span></span> | <span data-ttu-id="aadbb-120">Value</span><span class="sxs-lookup"><span data-stu-id="aadbb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aadbb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aadbb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aadbb-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="aadbb-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="aadbb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aadbb-123">Library</span></span><br/> | <dl> <span data-ttu-id="aadbb-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="aadbb-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aadbb-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aadbb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aadbb-126">**IPortableDeviceValuesCollection (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="aadbb-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




