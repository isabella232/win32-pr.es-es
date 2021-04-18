---
description: El método GetBufferFromIPortableDeviceValues serializa una interfaz IPortableDeviceValues enviada a una matriz de bytes asignada. La matriz de bytes devuelta se asigna al llamador y debe liberarla el llamador mediante CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer:: GetBufferFromIPortableDeviceValues (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718627"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="e0558-104">IWpdSerializer:: GetBufferFromIPortableDeviceValues (método)</span><span class="sxs-lookup"><span data-stu-id="e0558-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="e0558-105">El método **GetBufferFromIPortableDeviceValues** serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada.</span><span class="sxs-lookup"><span data-stu-id="e0558-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="e0558-106">La matriz de bytes devuelta se asigna al llamador y debe liberarla el llamador mediante **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="e0558-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0558-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0558-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="e0558-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0558-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0558-109">*pSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0558-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0558-110">Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que se va a serializar.</span><span class="sxs-lookup"><span data-stu-id="e0558-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="e0558-111">*ppBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0558-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0558-112">Puntero a un **byte \* *_ que contiene los datos serializados. Dispositivos portátiles de Windows asigna esta memoria; el autor de la llamada debe liberarlo llamando a _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="e0558-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="e0558-113">*pdwBufferSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0558-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0558-114">Puntero a un **valor DWORD** que especifica el tamaño del búfer asignado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e0558-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0558-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0558-115">Return value</span></span>

<span data-ttu-id="e0558-116">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0558-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e0558-117">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e0558-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e0558-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0558-118">Return code</span></span>                                                                                   | <span data-ttu-id="e0558-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0558-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0558-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0558-121">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e0558-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="e0558-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0558-123">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="e0558-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="e0558-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0558-125">No había suficiente memoria disponible para crear el búfer.</span><span class="sxs-lookup"><span data-stu-id="e0558-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e0558-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0558-126">Requirements</span></span>



| <span data-ttu-id="e0558-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0558-127">Requirement</span></span> | <span data-ttu-id="e0558-128">Value</span><span class="sxs-lookup"><span data-stu-id="e0558-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0558-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0558-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e0558-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0558-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0558-131">Library</span></span><br/> | <dl> <span data-ttu-id="e0558-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0558-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0558-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0558-134">**Interfaz IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="e0558-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




