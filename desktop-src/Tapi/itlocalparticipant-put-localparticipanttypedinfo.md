---
description: El \_ método put LocalParticipantTypedInfo establece la información del participante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant: método de ut_LocalParticipantTypedInfo de:p (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690648"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="5f503-103">ITLocalParticipant::p \_ método LocalParticipantTypedInfo UT</span><span class="sxs-lookup"><span data-stu-id="5f503-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="5f503-104">El método **Put \_ LocalParticipantTypedInfo** establece la información del participante.</span><span class="sxs-lookup"><span data-stu-id="5f503-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f503-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f503-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5f503-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f503-107">*InfoType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f503-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f503-108">[**Participante \_ Identificador de \_ información con tipo**](participant-typed-info.md) del tipo de información necesaria.</span><span class="sxs-lookup"><span data-stu-id="5f503-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="5f503-109">*ppInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f503-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f503-110">**BSTR** que contiene el nuevo valor necesario para la información.</span><span class="sxs-lookup"><span data-stu-id="5f503-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f503-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f503-111">Return value</span></span>

<span data-ttu-id="5f503-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5f503-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f503-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f503-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f503-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f503-114">Remarks</span></span>

<span data-ttu-id="5f503-115">La aplicación debe usar [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PpInfo* y usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="5f503-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f503-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f503-116">Requirements</span></span>



| <span data-ttu-id="5f503-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f503-117">Requirement</span></span> | <span data-ttu-id="5f503-118">Value</span><span class="sxs-lookup"><span data-stu-id="5f503-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f503-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5f503-119">TAPI version</span></span><br/> | <span data-ttu-id="5f503-120">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5f503-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5f503-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f503-121">Header</span></span><br/>       | <dl> <span data-ttu-id="5f503-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f503-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5f503-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f503-123">Library</span></span><br/>      | <dl> <span data-ttu-id="5f503-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f503-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5f503-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f503-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="5f503-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f503-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5f503-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f503-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f503-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="5f503-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="5f503-129">**\_información con tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

