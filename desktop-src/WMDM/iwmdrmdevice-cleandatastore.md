---
title: IWMDRMDevice CleanDataStore, método
description: El método CleanDataStore inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Método CleanDataStore de Windows Media Administrador de dispositivos
- Método CleanDataStore de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698517"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="25f74-106">IWMDRMDevice:: CleanDataStore (método)</span><span class="sxs-lookup"><span data-stu-id="25f74-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="25f74-107">El método **CleanDataStore** inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25f74-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f74-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25f74-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="25f74-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25f74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f74-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25f74-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f74-111">Marcas para los criterios de limpieza del almacén.</span><span class="sxs-lookup"><span data-stu-id="25f74-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f74-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25f74-112">Return value</span></span>

<span data-ttu-id="25f74-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="25f74-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="25f74-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="25f74-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="25f74-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25f74-115">Return code</span></span>                                                                          | <span data-ttu-id="25f74-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f74-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="25f74-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="25f74-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="25f74-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25f74-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f74-119">Requirements</span></span>



| <span data-ttu-id="25f74-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f74-120">Requirement</span></span> | <span data-ttu-id="25f74-121">Value</span><span class="sxs-lookup"><span data-stu-id="25f74-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f74-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25f74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="25f74-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="25f74-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25f74-124">Library</span></span><br/> | <dl> <span data-ttu-id="25f74-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f74-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="25f74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f74-127">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="25f74-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





