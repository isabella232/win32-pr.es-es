---
title: Método IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: El método ProcessLicenseDeletion elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Método ProcessLicenseDeletionMessage formato de Windows Media
- Método ProcessLicenseDeletionMessage formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718752"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="04633-106">IWMDRMLicenseManagement::P método rocessLicenseDeletionMessage</span><span class="sxs-lookup"><span data-stu-id="04633-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="04633-107">El método **ProcessLicenseDeletion** elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.</span><span class="sxs-lookup"><span data-stu-id="04633-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="04633-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04633-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="04633-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04633-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04633-110">*bstrDeletionMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04633-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04633-111">Mensaje que identifica la licencia que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="04633-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04633-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04633-112">Return value</span></span>

<span data-ttu-id="04633-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04633-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="04633-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="04633-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="04633-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="04633-115">Return code</span></span>                                                                          | <span data-ttu-id="04633-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="04633-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="04633-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="04633-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="04633-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="04633-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04633-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04633-119">Remarks</span></span>

<span data-ttu-id="04633-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="04633-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="04633-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04633-121">Requirements</span></span>



| <span data-ttu-id="04633-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="04633-122">Requirement</span></span> | <span data-ttu-id="04633-123">Value</span><span class="sxs-lookup"><span data-stu-id="04633-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04633-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04633-124">Header</span></span><br/> | <dl> <span data-ttu-id="04633-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="04633-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04633-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="04633-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04633-127">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="04633-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





