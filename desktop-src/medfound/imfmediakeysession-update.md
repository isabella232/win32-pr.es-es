---
description: Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMFMediaKeySession:: Update (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670091"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="baa2a-103">IMFMediaKeySession:: Update (método)</span><span class="sxs-lookup"><span data-stu-id="baa2a-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="baa2a-104">Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="baa2a-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baa2a-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="baa2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baa2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa2a-107">*key*</span><span class="sxs-lookup"><span data-stu-id="baa2a-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="baa2a-108">*CB*</span><span class="sxs-lookup"><span data-stu-id="baa2a-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="baa2a-109">El recuento en bytes de la *clave*.</span><span class="sxs-lookup"><span data-stu-id="baa2a-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa2a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baa2a-110">Return value</span></span>

<span data-ttu-id="baa2a-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="baa2a-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="baa2a-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="baa2a-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa2a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baa2a-113">Requirements</span></span>



| <span data-ttu-id="baa2a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa2a-114">Requirement</span></span> | <span data-ttu-id="baa2a-115">Value</span><span class="sxs-lookup"><span data-stu-id="baa2a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa2a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baa2a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="baa2a-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="baa2a-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="baa2a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baa2a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="baa2a-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="baa2a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="baa2a-120">IDL</span><span class="sxs-lookup"><span data-stu-id="baa2a-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="baa2a-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="baa2a-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa2a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="baa2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa2a-123">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="baa2a-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




