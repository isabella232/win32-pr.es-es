---
title: Mensaje de ICM_CONFIGURE (VFW. h)
description: El \_ mensaje configurar de ICM notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo de configuración o consulta un controlador de compresión de vídeo para determinar si tiene un cuadro de diálogo de configuración.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- Mensaje de ICM_CONFIGURE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676898"
---
# <a name="icm_configure-message"></a><span data-ttu-id="f0d97-104">\_Configurar mensaje de ICM</span><span class="sxs-lookup"><span data-stu-id="f0d97-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="f0d97-105">El **mensaje \_ configurar de ICM** notifica a un controlador de compresión de vídeo que muestre su cuadro de diálogo de configuración o consulta un controlador de compresión de vídeo para determinar si tiene un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="f0d97-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="f0d97-106">Puede enviar este mensaje explícitamente o mediante la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .</span><span class="sxs-lookup"><span data-stu-id="f0d97-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="f0d97-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0d97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d97-108"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="f0d97-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="f0d97-109">Identificador de la ventana primaria del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="f0d97-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="f0d97-110">Puede determinar si un controlador tiene un cuadro de diálogo de configuración especificando 1 en este parámetro, como en la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .</span><span class="sxs-lookup"><span data-stu-id="f0d97-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d97-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0d97-111">Return Value</span></span>

<span data-ttu-id="f0d97-112">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f0d97-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0d97-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0d97-113">Remarks</span></span>

<span data-ttu-id="f0d97-114">Este mensaje es diferente del mensaje [**de \_ configuración de DRV**](drv-configure.md) que se usa para la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="f0d97-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="f0d97-115">El cuadro de diálogo de este mensaje debe permitir que el usuario establezca y edite el estado interno al que hacen referencia los mensajes [**ICM \_ GETSTATE**](icm-getstate.md) y [**ICM \_ SETSTATE**](icm-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d97-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="f0d97-116">Por ejemplo, este cuadro de diálogo puede permitir que el usuario cambie los parámetros que afectan al nivel de calidad y otras opciones de compresión similares.</span><span class="sxs-lookup"><span data-stu-id="f0d97-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d97-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0d97-117">Requirements</span></span>



| <span data-ttu-id="f0d97-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d97-118">Requirement</span></span> | <span data-ttu-id="f0d97-119">Value</span><span class="sxs-lookup"><span data-stu-id="f0d97-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0d97-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0d97-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d97-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f0d97-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f0d97-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0d97-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d97-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0d97-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f0d97-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0d97-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d97-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d97-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d97-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0d97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d97-127">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f0d97-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f0d97-128">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f0d97-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





