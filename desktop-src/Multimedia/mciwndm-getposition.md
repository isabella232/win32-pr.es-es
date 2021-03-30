---
title: Mensaje de MCIWNDM_GETPOSITION (VFW. h)
description: El \_ mensaje MCIWNDM GETPOSITION recupera el valor numérico de la posición actual en el contenido del dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- Mensaje de MCIWNDM_GETPOSITION de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905054"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="f7cbe-104">Mensaje de MCIWNDM \_ GETPOSITION</span><span class="sxs-lookup"><span data-stu-id="f7cbe-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="f7cbe-105">El mensaje **MCIWNDM \_ GETPOSITION** recupera el valor numérico de la posición actual en el contenido del dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="f7cbe-106">Esta macro también proporciona la posición actual en forma de cadena en un búfer definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="f7cbe-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="f7cbe-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="f7cbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7cbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7cbe-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="f7cbe-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="f7cbe-110">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="f7cbe-111">Si la cadena terminada en NULL es más larga que el búfer, se trunca.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="f7cbe-112">Use cero para impedir la recuperación de la posición como una cadena.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="f7cbe-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="f7cbe-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="f7cbe-114">Puntero a un búfer definido por la aplicación que se usa para devolver la posición.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="f7cbe-115">Use cero para impedir la recuperación de la posición como una cadena.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="f7cbe-116">Si el dispositivo admite pistas, se devuelve la información de posición de cadena con el formato TT: MM: SS: FF, donde TT corresponde a las pistas, MM y SS corresponden a minutos y segundos, y FF corresponde a fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7cbe-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7cbe-117">Return Value</span></span>

<span data-ttu-id="f7cbe-118">Devuelve un entero que corresponde a la posición actual.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="f7cbe-119">Las unidades para el valor de posición dependen del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="f7cbe-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cbe-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7cbe-120">Requirements</span></span>



| <span data-ttu-id="f7cbe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7cbe-121">Requirement</span></span> | <span data-ttu-id="f7cbe-122">Value</span><span class="sxs-lookup"><span data-stu-id="f7cbe-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f7cbe-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7cbe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f7cbe-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f7cbe-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f7cbe-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7cbe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f7cbe-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7cbe-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f7cbe-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7cbe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7cbe-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7cbe-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7cbe-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7cbe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7cbe-130">**MCIWndGetPosition**</span><span class="sxs-lookup"><span data-stu-id="f7cbe-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="f7cbe-131">**MCIWndGetPositionString**</span><span class="sxs-lookup"><span data-stu-id="f7cbe-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





