---
description: Obtiene la clave que se usa para cifrar los mensajes salientes que protege el token.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'IUpdateEndpointAuthToken:: SigningKey (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082175"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="99bc1-103">IUpdateEndpointAuthToken:: SigningKey (método)</span><span class="sxs-lookup"><span data-stu-id="99bc1-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="99bc1-104">Obtiene la clave que se usa para cifrar los mensajes salientes que protege el token.</span><span class="sxs-lookup"><span data-stu-id="99bc1-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99bc1-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="99bc1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99bc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bc1-107">*pbKey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99bc1-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc1-108">Clave usada para cifrar el mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="99bc1-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="99bc1-109">*pcbKeySize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99bc1-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc1-110">Tamaño de la clave a la que hace referencia el parámetros de *pbkey* .</span><span class="sxs-lookup"><span data-stu-id="99bc1-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bc1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99bc1-111">Return value</span></span>

<span data-ttu-id="99bc1-112">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="99bc1-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="99bc1-113">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="99bc1-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bc1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99bc1-114">Requirements</span></span>



| <span data-ttu-id="99bc1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="99bc1-115">Requirement</span></span> | <span data-ttu-id="99bc1-116">Value</span><span class="sxs-lookup"><span data-stu-id="99bc1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99bc1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99bc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="99bc1-118">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="99bc1-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="99bc1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99bc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="99bc1-120">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="99bc1-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="99bc1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99bc1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="99bc1-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="99bc1-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="99bc1-123">IDL</span><span class="sxs-lookup"><span data-stu-id="99bc1-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99bc1-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99bc1-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="99bc1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99bc1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="99bc1-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99bc1-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="99bc1-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99bc1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99bc1-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99bc1-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99bc1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="99bc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bc1-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="99bc1-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




