---
description: Obtiene el objeto de claves multimedia asociado al motor multimedia o null si no hay un objeto de claves multimedia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMFMediaEngineEME:: get_Keys (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717390"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="67ccd-103">IMFMediaEngineEME:: get \_ Keys (método)</span><span class="sxs-lookup"><span data-stu-id="67ccd-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="67ccd-104">Obtiene el objeto de claves multimedia asociado al motor multimedia o **null** si no hay un objeto de claves multimedia.</span><span class="sxs-lookup"><span data-stu-id="67ccd-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ccd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67ccd-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="67ccd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ccd-107">*mykeys*</span><span class="sxs-lookup"><span data-stu-id="67ccd-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="67ccd-108">Objeto de claves multimedia asociado al motor multimedia o **null** si no hay un objeto de claves multimedia.</span><span class="sxs-lookup"><span data-stu-id="67ccd-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ccd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67ccd-109">Return value</span></span>

<span data-ttu-id="67ccd-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="67ccd-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67ccd-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67ccd-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ccd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ccd-112">Requirements</span></span>



| <span data-ttu-id="67ccd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ccd-113">Requirement</span></span> | <span data-ttu-id="67ccd-114">Value</span><span class="sxs-lookup"><span data-stu-id="67ccd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ccd-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ccd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="67ccd-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="67ccd-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="67ccd-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ccd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="67ccd-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="67ccd-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="67ccd-119">IDL</span><span class="sxs-lookup"><span data-stu-id="67ccd-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67ccd-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67ccd-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ccd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="67ccd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ccd-122">**IMFMediaEngineEME**</span><span class="sxs-lookup"><span data-stu-id="67ccd-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




