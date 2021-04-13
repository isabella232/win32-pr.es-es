---
title: Mensaje de ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: El \_ mensaje ICM Draw \_ SUGGESTFORMAT consulta un controlador de representación para sugerir un formato descomprimido que se puede dibujar.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- Mensaje de ICM_DRAW_SUGGESTFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489593"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="5fa06-104">\_Mensaje SUGGESTFORMAT de Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="5fa06-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="5fa06-105">El mensaje **ICM \_ Draw \_ SUGGESTFORMAT** consulta un controlador de representación para sugerir un formato descomprimido que se puede dibujar.</span><span class="sxs-lookup"><span data-stu-id="5fa06-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="5fa06-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fa06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa06-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span><span class="sxs-lookup"><span data-stu-id="5fa06-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="5fa06-108">Puntero a una estructura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .</span><span class="sxs-lookup"><span data-stu-id="5fa06-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5fa06-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fa06-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5fa06-110">Tamaño, en bytes, de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span><span class="sxs-lookup"><span data-stu-id="5fa06-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa06-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fa06-111">Return Value</span></span>

<span data-ttu-id="5fa06-112">Devuelve ICERR \_ OK si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5fa06-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="5fa06-113">Si el miembro **lpbiSuggest** de la estructura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) es **null**, este mensaje devuelve la cantidad de memoria necesaria para contener el formato sugerido.</span><span class="sxs-lookup"><span data-stu-id="5fa06-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa06-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fa06-114">Remarks</span></span>

<span data-ttu-id="5fa06-115">El controlador debe examinar el formato especificado en el miembro **lpbiIn** de la estructura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) y usar el miembro **lpbiSuggest** para devolver un formato que pueda dibujar.</span><span class="sxs-lookup"><span data-stu-id="5fa06-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="5fa06-116">El formato de salida debe conservar tantos datos como sea posible desde el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fa06-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="5fa06-117">Opcionalmente, el controlador puede usar el controlador de compresor instalable pasado en el miembro **hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) para realizar selecciones más complejas.</span><span class="sxs-lookup"><span data-stu-id="5fa06-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="5fa06-118">Por ejemplo, si el formato de entrada es datos JPEG de 24 bits, un representador podría consultar el descompresor para averiguar si se puede descomprimir en un formato YUV (que podría dibujarse más eficazmente) antes de seleccionar el formato que se va a sugerir.</span><span class="sxs-lookup"><span data-stu-id="5fa06-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa06-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fa06-119">Requirements</span></span>



| <span data-ttu-id="5fa06-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa06-120">Requirement</span></span> | <span data-ttu-id="5fa06-121">Value</span><span class="sxs-lookup"><span data-stu-id="5fa06-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fa06-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fa06-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa06-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5fa06-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5fa06-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fa06-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa06-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5fa06-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5fa06-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fa06-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fa06-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fa06-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa06-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fa06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa06-129">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="5fa06-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5fa06-130">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="5fa06-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





