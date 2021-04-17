---
title: IWMDRMDevice GetSecureClockChallenge, método
description: El método GetSecureClockChallenge recupera el resultado del desafío de reloj seguro.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Método GetSecureClockChallenge de Windows Media Administrador de dispositivos
- Método GetSecureClockChallenge de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698506"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="96f05-106">IWMDRMDevice:: GetSecureClockChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="96f05-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="96f05-107">El método **GetSecureClockChallenge** recupera el resultado del desafío de reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="96f05-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f05-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96f05-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="96f05-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96f05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96f05-110">*ppbChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96f05-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96f05-111">Resultado de desafío recuperado.</span><span class="sxs-lookup"><span data-stu-id="96f05-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="96f05-112">*pcbChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96f05-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96f05-113">Tamaño del resultado del desafío, en bytes.</span><span class="sxs-lookup"><span data-stu-id="96f05-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96f05-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96f05-114">Return value</span></span>

<span data-ttu-id="96f05-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="96f05-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="96f05-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="96f05-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="96f05-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="96f05-117">Return code</span></span>                                                                          | <span data-ttu-id="96f05-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="96f05-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="96f05-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="96f05-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="96f05-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="96f05-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96f05-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96f05-121">Requirements</span></span>



| <span data-ttu-id="96f05-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f05-122">Requirement</span></span> | <span data-ttu-id="96f05-123">Value</span><span class="sxs-lookup"><span data-stu-id="96f05-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96f05-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96f05-124">Header</span></span><br/>  | <dl> <span data-ttu-id="96f05-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96f05-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="96f05-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96f05-126">Library</span></span><br/> | <dl> <span data-ttu-id="96f05-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96f05-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96f05-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96f05-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f05-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="96f05-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="96f05-130">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="96f05-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





