---
description: 'Método IPortableDeviceValues::GetCount: el método GetCount recupera el número de elementos de la colección.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: Método IPortableDeviceValues::GetCount (PortableDeviceTypes.h)
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
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086243"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="60aba-103">IPortableDeviceValues::GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="60aba-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="60aba-104">El **método GetCount** recupera el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="60aba-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60aba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60aba-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="60aba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60aba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60aba-107">*pcelt* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="60aba-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60aba-108">Puntero a un **DWORD** que contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="60aba-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60aba-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60aba-109">Return value</span></span>

<span data-ttu-id="60aba-110">El método devuelve un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="60aba-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60aba-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="60aba-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60aba-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60aba-112">Return code</span></span>                                                                          | <span data-ttu-id="60aba-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="60aba-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="60aba-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60aba-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60aba-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="60aba-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60aba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60aba-116">Requirements</span></span>



| <span data-ttu-id="60aba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="60aba-117">Requirement</span></span> | <span data-ttu-id="60aba-118">Value</span><span class="sxs-lookup"><span data-stu-id="60aba-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60aba-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60aba-119">Header</span></span><br/>  | <dl> <span data-ttu-id="60aba-120"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="60aba-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="60aba-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60aba-121">Library</span></span><br/> | <dl> <span data-ttu-id="60aba-122"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="60aba-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60aba-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60aba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60aba-124">**IPortableDeviceValues (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="60aba-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




