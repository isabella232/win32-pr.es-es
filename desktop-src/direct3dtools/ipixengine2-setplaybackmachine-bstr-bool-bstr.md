---
description: Establece el equipo de reproducción actual para el registro de gráficos especificado.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: SetPlaybackMachine (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538188"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="07a34-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2:: SetPlaybackMachine (método)</span><span class="sxs-lookup"><span data-stu-id="07a34-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="07a34-104">Establece el equipo de reproducción actual para el registro de gráficos especificado.</span><span class="sxs-lookup"><span data-stu-id="07a34-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07a34-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="07a34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07a34-106">Parameters</span></span>

<span data-ttu-id="07a34-107">*MSDTC* </span><span class="sxs-lookup"><span data-stu-id="07a34-107">*logFile* </span></span>  
<span data-ttu-id="07a34-108">Una cadena COM contianing el nombre del registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="07a34-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="07a34-109">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="07a34-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="07a34-110">True para utilizar la autenticación; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="07a34-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="07a34-111">*sistema* </span><span class="sxs-lookup"><span data-stu-id="07a34-111">*machine* </span></span>  
<span data-ttu-id="07a34-112">Cadena COM que contiene el nombre del equipo de reproducción.</span><span class="sxs-lookup"><span data-stu-id="07a34-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="07a34-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07a34-113">Return value</span></span>

<span data-ttu-id="07a34-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="07a34-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07a34-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07a34-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a34-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07a34-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="07a34-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07a34-117">Header</span></span></p></td><td><span data-ttu-id="07a34-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="07a34-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="07a34-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="07a34-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="07a34-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="07a34-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
