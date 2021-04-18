---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: El método CreateLicenseRevocationChallenge genera un desafío de revocación de licencia.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Método CreateLicenseRevocationChallenge formato de Windows Media
- Método CreateLicenseRevocationChallenge formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718765"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="97beb-106">IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="97beb-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="97beb-107">El método **CreateLicenseRevocationChallenge** genera un desafío de revocación de licencia.</span><span class="sxs-lookup"><span data-stu-id="97beb-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="97beb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97beb-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="97beb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97beb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97beb-110">*pbMachineID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97beb-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-111">Identificador de equipo especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="97beb-111">User-specified machine identifier.</span></span> <span data-ttu-id="97beb-112">Este valor se utiliza para consultar una licencia en el servidor y debe ajustarse al formato que use el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="97beb-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="97beb-113">*cbMachineID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97beb-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-114">Tamaño, en bytes, del identificador de la máquina.</span><span class="sxs-lookup"><span data-stu-id="97beb-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="97beb-115">*pbChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97beb-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-116">Datos de desafío especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="97beb-116">User-specified challenge data.</span></span> <span data-ttu-id="97beb-117">Estos datos, además del identificador de equipo, se usan para consultar el servidor de licencias para obtener las licencias que se van a revocar.</span><span class="sxs-lookup"><span data-stu-id="97beb-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="97beb-118">*cbChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97beb-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-119">Tamaño, en bytes, de los datos de desafío.</span><span class="sxs-lookup"><span data-stu-id="97beb-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="97beb-120">*ppbChallengeOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="97beb-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-121">Dirección de un puntero que recibe la dirección de la salida del desafío.</span><span class="sxs-lookup"><span data-stu-id="97beb-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="97beb-122">Este búfer son los datos que se envían al servicio de revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="97beb-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="97beb-123">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="97beb-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="97beb-124">*pcbChallengeOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="97beb-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97beb-125">Dirección de una variable que recibe el tamaño de los datos de salida de desafío asignados, en bytes.</span><span class="sxs-lookup"><span data-stu-id="97beb-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97beb-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97beb-126">Return value</span></span>

<span data-ttu-id="97beb-127">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="97beb-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="97beb-128">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="97beb-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="97beb-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="97beb-129">Return code</span></span>                                                                          | <span data-ttu-id="97beb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="97beb-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="97beb-131"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="97beb-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="97beb-132">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="97beb-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97beb-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97beb-133">Remarks</span></span>

<span data-ttu-id="97beb-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="97beb-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="97beb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97beb-135">Requirements</span></span>



| <span data-ttu-id="97beb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="97beb-136">Requirement</span></span> | <span data-ttu-id="97beb-137">Value</span><span class="sxs-lookup"><span data-stu-id="97beb-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97beb-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97beb-138">Header</span></span><br/> | <dl> <span data-ttu-id="97beb-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="97beb-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97beb-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="97beb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97beb-141">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="97beb-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





