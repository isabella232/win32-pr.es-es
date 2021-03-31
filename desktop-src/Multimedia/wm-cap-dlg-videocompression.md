---
title: Mensaje de WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: El \_ \_ \_ mensaje de compresión de videocompresión de Cap de WM muestra un cuadro de diálogo en el que el usuario puede seleccionar un compresor para usarlo durante el proceso de captura.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Mensaje de WM_CAP_DLG_VIDEOCOMPRESSION de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079341"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="c5f4b-104">\_Mensaje de \_ compresión de \_ videocompresión de Cap de WM</span><span class="sxs-lookup"><span data-stu-id="c5f4b-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="c5f4b-105">El mensaje de **\_ compresión de \_ \_ videocompresión de Cap de WM** muestra un cuadro de diálogo en el que el usuario puede seleccionar un compresor para usarlo durante el proceso de captura.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="c5f4b-106">La lista de compresores disponibles puede variar con el formato de vídeo seleccionado en el cuadro de diálogo formato de vídeo del controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="c5f4b-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="c5f4b-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="c5f4b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5f4b-108">Return Value</span></span>

<span data-ttu-id="c5f4b-109">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f4b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5f4b-110">Remarks</span></span>

<span data-ttu-id="c5f4b-111">Use este mensaje con controladores de captura que proporcionen fotogramas solo en \_ formato RGB de BI.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="c5f4b-112">Este mensaje es muy útil en la operación de captura por pasos para combinar la captura y la compresión en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="c5f4b-113">Es muy probable que la compresión de fotogramas con un compresor de software como parte de una operación de captura en tiempo real sea demasiado lenta.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="c5f4b-114">La compresión no afecta a los fotogramas copiados en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c5f4b-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f4b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5f4b-115">Requirements</span></span>



| <span data-ttu-id="c5f4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f4b-116">Requirement</span></span> | <span data-ttu-id="c5f4b-117">Value</span><span class="sxs-lookup"><span data-stu-id="c5f4b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5f4b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f4b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f4b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5f4b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5f4b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f4b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f4b-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5f4b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5f4b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5f4b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5f4b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f4b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f4b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5f4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f4b-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5f4b-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c5f4b-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5f4b-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





