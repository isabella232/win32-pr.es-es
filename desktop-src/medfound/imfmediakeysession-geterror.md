---
description: Obtiene el estado de error asociado a la sesión de la clave multimedia.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'IMFMediaKeySession:: GetError (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721359"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="0e701-103">IMFMediaKeySession:: GetError (método)</span><span class="sxs-lookup"><span data-stu-id="0e701-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="0e701-104">Obtiene el estado de error asociado a la sesión de la clave multimedia.</span><span class="sxs-lookup"><span data-stu-id="0e701-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e701-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e701-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="0e701-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e701-107">*code*</span><span class="sxs-lookup"><span data-stu-id="0e701-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="0e701-108">Código de error.</span><span class="sxs-lookup"><span data-stu-id="0e701-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="0e701-109">*systemCode*</span><span class="sxs-lookup"><span data-stu-id="0e701-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="0e701-110">Información de error específica de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0e701-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e701-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e701-111">Return value</span></span>

<span data-ttu-id="0e701-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0e701-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e701-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e701-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e701-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e701-114">Requirements</span></span>



| <span data-ttu-id="0e701-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e701-115">Requirement</span></span> | <span data-ttu-id="0e701-116">Value</span><span class="sxs-lookup"><span data-stu-id="0e701-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e701-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e701-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e701-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0e701-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e701-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e701-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e701-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e701-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0e701-121">IDL</span><span class="sxs-lookup"><span data-stu-id="0e701-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0e701-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0e701-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e701-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e701-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e701-124">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="0e701-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




