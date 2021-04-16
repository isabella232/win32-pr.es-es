---
description: Se utiliza para indicar que se ha producido un error con el búfer de origen.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'IMFSourceBufferNotify:: OnError (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705805"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="b1e7e-103">IMFSourceBufferNotify:: OnError (método)</span><span class="sxs-lookup"><span data-stu-id="b1e7e-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="b1e7e-104">Se utiliza para indicar que se ha producido un error con el búfer de origen.</span><span class="sxs-lookup"><span data-stu-id="b1e7e-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1e7e-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="b1e7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e7e-107">*HR* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1e7e-107">*hr* \[in\]</span></span>
<span data-ttu-id="b1e7e-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b1e7e-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b1e7e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1e7e-109">Return value</span></span>

<span data-ttu-id="b1e7e-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b1e7e-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e7e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e7e-111">Requirements</span></span>



| <span data-ttu-id="b1e7e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e7e-112">Requirement</span></span> | <span data-ttu-id="b1e7e-113">Value</span><span class="sxs-lookup"><span data-stu-id="b1e7e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e7e-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e7e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e7e-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b1e7e-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1e7e-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e7e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e7e-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e7e-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b1e7e-118">IDL</span><span class="sxs-lookup"><span data-stu-id="b1e7e-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1e7e-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1e7e-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e7e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1e7e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e7e-121">**IMFSourceBufferNotify**</span><span class="sxs-lookup"><span data-stu-id="b1e7e-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




