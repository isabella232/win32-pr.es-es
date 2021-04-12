---
description: Determina si un dispositivo de entrada es compatible con multitoque.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3:: IsMultiTouch (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278476"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="1d0cc-103">ITablet3:: IsMultiTouch (método)</span><span class="sxs-lookup"><span data-stu-id="1d0cc-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="1d0cc-104">Determina si un dispositivo de entrada es compatible con multitoque.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d0cc-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="1d0cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d0cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0cc-107">*bIsMultiTouch* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1d0cc-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0cc-108">Indica si el dispositivo es multitoque.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0cc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d0cc-109">Return value</span></span>

<span data-ttu-id="1d0cc-110">Devuelve **si \_ es** correcto; de lo contrario, devuelve un código de error como **E \_**.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0cc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d0cc-111">Remarks</span></span>

<span data-ttu-id="1d0cc-112">Después de determinar a través de [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3:: IsMultiTouch** que multitoque está disponible, una aplicación puede optar por participar en los mensajes de entrada de multitoque.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="1d0cc-113">Puede encontrar información adicional sobre cómo filtrar métodos multitoque en la sección de propiedades **IRealTimeStylus3:: MultiTouchEnabled** .</span><span class="sxs-lookup"><span data-stu-id="1d0cc-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="1d0cc-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1d0cc-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="1d0cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0cc-115">Requirements</span></span>



| <span data-ttu-id="1d0cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0cc-116">Requirement</span></span> | <span data-ttu-id="1d0cc-117">Value</span><span class="sxs-lookup"><span data-stu-id="1d0cc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0cc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d0cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0cc-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d0cc-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1d0cc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d0cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0cc-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d0cc-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1d0cc-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d0cc-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d0cc-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d0cc-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0cc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d0cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0cc-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="1d0cc-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




