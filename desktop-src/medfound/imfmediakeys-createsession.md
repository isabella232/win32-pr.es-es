---
description: Crea un objeto de sesión de clave multimedia con los datos de inicialización y los datos personalizados especificados. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMFMediaKeys:: CreateSession (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697967"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="9867c-104">IMFMediaKeys:: CreateSession (método)</span><span class="sxs-lookup"><span data-stu-id="9867c-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="9867c-105">Crea un objeto de sesión de clave multimedia con los datos de inicialización y los datos personalizados especificados.</span><span class="sxs-lookup"><span data-stu-id="9867c-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="9867c-106">.</span><span class="sxs-lookup"><span data-stu-id="9867c-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="9867c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9867c-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="9867c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9867c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9867c-109">*mimeType*</span><span class="sxs-lookup"><span data-stu-id="9867c-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-110">El tipo MIME del contenedor multimedia utilizado para el contenido.</span><span class="sxs-lookup"><span data-stu-id="9867c-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="9867c-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="9867c-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-112">Los datos de inicialización del sistema de claves.</span><span class="sxs-lookup"><span data-stu-id="9867c-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="9867c-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="9867c-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-114">El recuento en bytes de *initData*.</span><span class="sxs-lookup"><span data-stu-id="9867c-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="9867c-115">*customData*</span><span class="sxs-lookup"><span data-stu-id="9867c-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-116">Datos personalizados enviados al sistema de claves.</span><span class="sxs-lookup"><span data-stu-id="9867c-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="9867c-117">*cbCustomData*</span><span class="sxs-lookup"><span data-stu-id="9867c-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-118">El recuento en bytes de *cbCustomData*.</span><span class="sxs-lookup"><span data-stu-id="9867c-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="9867c-119">*notificar a*</span><span class="sxs-lookup"><span data-stu-id="9867c-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-120">notificar a</span><span class="sxs-lookup"><span data-stu-id="9867c-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="9867c-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="9867c-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="9867c-122">La sesión de la clave multimedia.</span><span class="sxs-lookup"><span data-stu-id="9867c-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9867c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9867c-123">Return value</span></span>

<span data-ttu-id="9867c-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9867c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9867c-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9867c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9867c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9867c-126">Requirements</span></span>



| <span data-ttu-id="9867c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9867c-127">Requirement</span></span> | <span data-ttu-id="9867c-128">Value</span><span class="sxs-lookup"><span data-stu-id="9867c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9867c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9867c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9867c-130">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9867c-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9867c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9867c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9867c-132">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9867c-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9867c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="9867c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9867c-134"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9867c-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9867c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9867c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9867c-136">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="9867c-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




