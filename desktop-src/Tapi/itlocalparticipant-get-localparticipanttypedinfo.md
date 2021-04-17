---
description: El \_ método get LocalParticipantTypedInfo obtiene información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Método ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690650"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="98328-103">ITLocalParticipant:: get \_ LocalParticipantTypedInfo (método)</span><span class="sxs-lookup"><span data-stu-id="98328-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="98328-104">El método **Get \_ LocalParticipantTypedInfo** obtiene información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="98328-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="98328-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98328-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="98328-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98328-107">*InfoType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98328-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98328-108">[**Participante \_ Identificador de \_ información con tipo**](participant-typed-info.md) de tipo de información requerida.</span><span class="sxs-lookup"><span data-stu-id="98328-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="98328-109">*ppInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="98328-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98328-110">Puntero a un **BSTR** que contendrá la información necesaria después de una devolución correcta del método.</span><span class="sxs-lookup"><span data-stu-id="98328-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98328-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98328-111">Return value</span></span>

<span data-ttu-id="98328-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="98328-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98328-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98328-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98328-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98328-114">Remarks</span></span>

<span data-ttu-id="98328-115">La aplicación debe usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="98328-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="98328-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98328-116">Requirements</span></span>



| <span data-ttu-id="98328-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98328-117">Requirement</span></span> | <span data-ttu-id="98328-118">Value</span><span class="sxs-lookup"><span data-stu-id="98328-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98328-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="98328-119">TAPI version</span></span><br/> | <span data-ttu-id="98328-120">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="98328-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="98328-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98328-121">Header</span></span><br/>       | <dl> <span data-ttu-id="98328-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="98328-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="98328-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98328-123">Library</span></span><br/>      | <dl> <span data-ttu-id="98328-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98328-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="98328-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98328-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="98328-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98328-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="98328-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="98328-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98328-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="98328-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="98328-129">**\_información con tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="98328-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

