---
title: IWMDRMLicense GetOutputProtectionLevels, método
description: El método GetOutputProtectionLevels recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Método GetOutputProtectionLevels formato de Windows Media
- Método GetOutputProtectionLevels formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704831"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="447a8-106">IWMDRMLicense:: GetOutputProtectionLevels (método)</span><span class="sxs-lookup"><span data-stu-id="447a8-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="447a8-107">El método **GetOutputProtectionLevels** recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.</span><span class="sxs-lookup"><span data-stu-id="447a8-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="447a8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="447a8-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="447a8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="447a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="447a8-110">*pOPLs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="447a8-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="447a8-111">Puntero a una estructura de [**\_ niveles de \_ protección \_ de salida WMDRM**](wmdrm-output-protection-levels.md) que recibe la información de OPL.</span><span class="sxs-lookup"><span data-stu-id="447a8-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="447a8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="447a8-112">Return value</span></span>

<span data-ttu-id="447a8-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="447a8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="447a8-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="447a8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="447a8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="447a8-115">Return code</span></span>                                                                          | <span data-ttu-id="447a8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="447a8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="447a8-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="447a8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="447a8-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="447a8-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="447a8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="447a8-119">Remarks</span></span>

<span data-ttu-id="447a8-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="447a8-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="447a8-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="447a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447a8-122">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="447a8-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





