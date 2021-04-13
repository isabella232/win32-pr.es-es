---
title: Mensaje de WM_CAP_FILE_SAVEAS (VFW. h)
description: El \_ \_ \_ mensaje de almacenamiento Cap de WM copia el contenido del archivo de captura en otro archivo. Puede enviar este mensaje explícitamente o mediante la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- Mensaje de WM_CAP_FILE_SAVEAS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422113"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="a2ed8-105">\_ \_ Mensaje SaveAs de archivo Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="a2ed8-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="a2ed8-106">El mensaje de **\_ \_ \_ almacenamiento Cap de WM** copia el contenido del archivo de captura en otro archivo.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="a2ed8-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .</span><span class="sxs-lookup"><span data-stu-id="a2ed8-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="a2ed8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2ed8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ed8-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="a2ed8-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="a2ed8-110">Puntero a la cadena terminada en null que contiene el nombre del archivo de destino que se usa para copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ed8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2ed8-111">Return Value</span></span>

<span data-ttu-id="a2ed8-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="a2ed8-113">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ed8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2ed8-114">Remarks</span></span>

<span data-ttu-id="a2ed8-115">Este mensaje no cambia el nombre o el contenido del archivo de captura actual.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="a2ed8-116">Si la operación de copia no se realiza correctamente debido a un error de disco lleno, el archivo de destino se eliminará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="a2ed8-117">Normalmente, un archivo de captura está preasignado para el segmento de captura más grande previsto y solo una parte de él podría usarse para capturar los datos.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="a2ed8-118">Este mensaje solo copia la parte del archivo que contiene los datos de captura.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ed8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ed8-119">Requirements</span></span>



| <span data-ttu-id="a2ed8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ed8-120">Requirement</span></span> | <span data-ttu-id="a2ed8-121">Value</span><span class="sxs-lookup"><span data-stu-id="a2ed8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a2ed8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2ed8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ed8-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2ed8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a2ed8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2ed8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ed8-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2ed8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a2ed8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2ed8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ed8-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed8-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ed8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2ed8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ed8-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="a2ed8-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a2ed8-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="a2ed8-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





