---
description: El método WriteIPortableDeviceValuesToBuffer serializa una interfaz IPortableDeviceValues a una matriz de bytes asignada por el llamador.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721571"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="3a1cb-103">IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="3a1cb-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="3a1cb-104">El método **WriteIPortableDeviceValuesToBuffer** serializa una interfaz **IPortableDeviceValues** a una matriz de bytes asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a1cb-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="3a1cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a1cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1cb-107">*dwOutputBufferLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a1cb-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1cb-108">**DWORD** que especifica el tamaño de *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a1cb-109">*pResults* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a1cb-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1cb-110">Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que se va a serializar.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="3a1cb-111">*pBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3a1cb-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1cb-112">Puntero a un búfer asignado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="3a1cb-113">Para obtener información sobre el tamaño del búfer necesario, llame a **GetSerializedSize**.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1cb-114">*pdwBytesWritten* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3a1cb-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1cb-115">Puntero a un **valor DWORD** que indica el número de bytes que se ha escrito realmente en el búfer asignado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1cb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a1cb-116">Return value</span></span>

<span data-ttu-id="3a1cb-117">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a1cb-118">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a1cb-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3a1cb-119">Return code</span></span>                                                                                   | <span data-ttu-id="3a1cb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a1cb-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="3a1cb-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1cb-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3a1cb-122">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="3a1cb-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1cb-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3a1cb-124">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="3a1cb-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1cb-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3a1cb-126">El búfer proporcionado por el autor de la llamada no era lo suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a1cb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a1cb-127">Remarks</span></span>

<span data-ttu-id="3a1cb-128">Este método copia una interfaz **IPortableDeviceValues** en un búfer existente.</span><span class="sxs-lookup"><span data-stu-id="3a1cb-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="3a1cb-129">Si desea asignar un nuevo búfer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a1cb-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1cb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a1cb-130">Requirements</span></span>



| <span data-ttu-id="3a1cb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a1cb-131">Requirement</span></span> | <span data-ttu-id="3a1cb-132">Value</span><span class="sxs-lookup"><span data-stu-id="3a1cb-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1cb-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a1cb-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1cb-134"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1cb-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a1cb-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a1cb-135">Library</span></span><br/> | <dl> <span data-ttu-id="3a1cb-136"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a1cb-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1cb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a1cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1cb-138">**Interfaz IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="3a1cb-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




