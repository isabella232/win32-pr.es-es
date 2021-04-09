---
description: Este método devuelve una interfaz que proporciona acceso a los datos de audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'IAudioFrameNative:: GetData (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154306"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="33047-103">IAudioFrameNative:: GetData (método)</span><span class="sxs-lookup"><span data-stu-id="33047-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="33047-104">Este método devuelve una interfaz que proporciona acceso a los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="33047-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="33047-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33047-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="33047-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33047-107">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33047-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33047-108">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="33047-108">Type: **REFIID**</span></span>

<span data-ttu-id="33047-109">IID de la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="33047-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="33047-110">*PPV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33047-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33047-111">Tipo: \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="33047-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="33047-112">Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en _riid parámetro \*.</span><span class="sxs-lookup"><span data-stu-id="33047-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33047-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33047-113">Return value</span></span>

<span data-ttu-id="33047-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33047-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33047-115">Devuelve S \_ correcto al finalizar correctamente.</span><span class="sxs-lookup"><span data-stu-id="33047-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="33047-116">Devuelve E \_ nointerface si no se encuentra la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="33047-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="33047-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="33047-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33047-118">**IAudioFrameNative**</span><span class="sxs-lookup"><span data-stu-id="33047-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



