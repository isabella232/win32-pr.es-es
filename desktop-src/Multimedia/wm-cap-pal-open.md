---
title: Mensaje de WM_CAP_PAL_OPEN (VFW. h)
description: El \_ \_ \_ mensaje abierto PAL Cap de WM carga una nueva paleta desde un archivo de paleta y la pasa a un controlador de captura.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- Mensaje de WM_CAP_PAL_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665929"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="3baae-104">\_ \_ Mensaje abierto PAL Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="3baae-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="3baae-105">El **mensaje \_ \_ \_ abierto PAL Cap de WM** carga una nueva paleta desde un archivo de paleta y la pasa a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="3baae-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="3baae-106">Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales.</span><span class="sxs-lookup"><span data-stu-id="3baae-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="3baae-107">Un controlador de captura usa una paleta cuando lo requiere el formato de imagen digitalizada especificado.</span><span class="sxs-lookup"><span data-stu-id="3baae-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="3baae-108">Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .</span><span class="sxs-lookup"><span data-stu-id="3baae-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="3baae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3baae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3baae-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="3baae-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="3baae-111">Puntero a una cadena terminada en null que contiene el nombre de archivo de la paleta.</span><span class="sxs-lookup"><span data-stu-id="3baae-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3baae-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3baae-112">Return Value</span></span>

<span data-ttu-id="3baae-113">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3baae-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="3baae-114">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="3baae-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="3baae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3baae-115">Requirements</span></span>



| <span data-ttu-id="3baae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3baae-116">Requirement</span></span> | <span data-ttu-id="3baae-117">Value</span><span class="sxs-lookup"><span data-stu-id="3baae-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3baae-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3baae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3baae-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3baae-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3baae-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3baae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3baae-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3baae-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3baae-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3baae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3baae-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3baae-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3baae-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3baae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3baae-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3baae-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3baae-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3baae-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





