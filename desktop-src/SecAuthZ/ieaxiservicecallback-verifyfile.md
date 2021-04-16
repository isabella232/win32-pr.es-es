---
description: Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'IeAxiServiceCallback:: VerifyFile (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546531"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="59cdf-103">IeAxiServiceCallback:: VerifyFile (método)</span><span class="sxs-lookup"><span data-stu-id="59cdf-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="59cdf-104">El método **VerifyFile** realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.</span><span class="sxs-lookup"><span data-stu-id="59cdf-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cdf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59cdf-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="59cdf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59cdf-107">*bstrFileUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59cdf-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cdf-108">Dirección URL del objeto ActiveX que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="59cdf-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="59cdf-109">*bstrApprovedFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="59cdf-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59cdf-110">Nombre del archivo donde se descargó el archivo. cab asociado al objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="59cdf-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59cdf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59cdf-111">Return value</span></span>

<span data-ttu-id="59cdf-112">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="59cdf-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="59cdf-113">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="59cdf-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="59cdf-114">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="59cdf-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="59cdf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59cdf-115">Requirements</span></span>



| <span data-ttu-id="59cdf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cdf-116">Requirement</span></span> | <span data-ttu-id="59cdf-117">Value</span><span class="sxs-lookup"><span data-stu-id="59cdf-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cdf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59cdf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59cdf-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="59cdf-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="59cdf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59cdf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59cdf-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="59cdf-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="59cdf-122">IID</span><span class="sxs-lookup"><span data-stu-id="59cdf-122">IID</span></span><br/>                      | <span data-ttu-id="59cdf-123">IID \_ IeAxiServiceCallback se define como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="59cdf-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="59cdf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="59cdf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59cdf-125">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="59cdf-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

