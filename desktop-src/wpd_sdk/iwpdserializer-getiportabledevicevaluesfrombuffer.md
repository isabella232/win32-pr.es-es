---
description: El método GetIPortableDeviceValuesFromBuffer deserializa una matriz de bytes en una interfaz IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670384"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="3ac6b-103">IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="3ac6b-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="3ac6b-104">El método **GetIPortableDeviceValuesFromBuffer** deserializa una matriz de bytes en una interfaz **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="3ac6b-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac6b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ac6b-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="3ac6b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ac6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac6b-107">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac6b-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac6b-108">Puntero al búfer que se va a deserializar.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="3ac6b-109">*dwInputBufferLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ac6b-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac6b-110">**DWORD** que especifica el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3ac6b-111">*ppParams* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3ac6b-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac6b-112">Dirección de una variable que recibe un puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) creada a partir del búfer.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="3ac6b-113">La aplicación es responsable de llamar a **Release** en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac6b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac6b-114">Return value</span></span>

<span data-ttu-id="3ac6b-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3ac6b-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3ac6b-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3ac6b-117">Return code</span></span>                                                                                  | <span data-ttu-id="3ac6b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ac6b-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3ac6b-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac6b-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3ac6b-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="3ac6b-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac6b-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3ac6b-122">Un argumento de puntero necesario era **null**.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="3ac6b-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac6b-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="3ac6b-124">Se produjo un error de conversión no especificado.</span><span class="sxs-lookup"><span data-stu-id="3ac6b-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ac6b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac6b-125">Requirements</span></span>



| <span data-ttu-id="3ac6b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac6b-126">Requirement</span></span> | <span data-ttu-id="3ac6b-127">Value</span><span class="sxs-lookup"><span data-stu-id="3ac6b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac6b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ac6b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3ac6b-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac6b-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ac6b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ac6b-130">Library</span></span><br/> | <dl> <span data-ttu-id="3ac6b-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ac6b-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac6b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ac6b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac6b-133">**Interfaz IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="3ac6b-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




