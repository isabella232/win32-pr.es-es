---
description: Obtiene un identificador de sesión único creado para esta sesión.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'IMFMediaKeySession:: get_SessionId (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670065"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="39f13-103">IMFMediaKeySession:: get \_ SessionID (método)</span><span class="sxs-lookup"><span data-stu-id="39f13-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="39f13-104">Obtiene un identificador de sesión único creado para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="39f13-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f13-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39f13-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="39f13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39f13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f13-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="39f13-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="39f13-108">Identificador de sesión de la clave multimedia.</span><span class="sxs-lookup"><span data-stu-id="39f13-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f13-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39f13-109">Return value</span></span>

<span data-ttu-id="39f13-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="39f13-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39f13-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39f13-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f13-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39f13-112">Requirements</span></span>



| <span data-ttu-id="39f13-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="39f13-113">Requirement</span></span> | <span data-ttu-id="39f13-114">Value</span><span class="sxs-lookup"><span data-stu-id="39f13-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f13-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39f13-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39f13-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="39f13-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39f13-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39f13-117">Minimum supported server</span></span><br/> | <span data-ttu-id="39f13-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39f13-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39f13-119">IDL</span><span class="sxs-lookup"><span data-stu-id="39f13-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39f13-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39f13-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f13-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="39f13-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f13-122">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="39f13-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




