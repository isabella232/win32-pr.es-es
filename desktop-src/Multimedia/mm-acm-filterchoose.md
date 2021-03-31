---
title: Mensaje de MM_ACM_FILTERCHOOSE (MSACM. h)
description: El \_ mensaje mm ACM \_ FILTERCHOOSE notifica a una función de enlace del cuadro de diálogo de acmFilterChoose antes de agregar un elemento a uno de los tres cuadros de lista desplegable.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- Mensaje de MM_ACM_FILTERCHOOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149972"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="df62c-104">\_ \_ Mensaje FILTERCHOOSE de mm ACM</span><span class="sxs-lookup"><span data-stu-id="df62c-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="df62c-105">El mensaje **mm \_ ACM \_ FILTERCHOOSE** notifica a una función de enlace del cuadro de diálogo de [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) antes de agregar un elemento a uno de los tres cuadros de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="df62c-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="df62c-106">Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="df62c-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="df62c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df62c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df62c-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="df62c-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="df62c-109">Cuadro de lista desplegable que se va a inicializar y una operación de comprobación o adición.</span><span class="sxs-lookup"><span data-stu-id="df62c-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="df62c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="df62c-110">Requirement</span></span> | <span data-ttu-id="df62c-111">Value</span><span class="sxs-lookup"><span data-stu-id="df62c-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df62c-112">\_comprobación personalizada de FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="df62c-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="df62c-113">El parámetro *lParam* es un puntero a una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable Nombre personalizado.</span><span class="sxs-lookup"><span data-stu-id="df62c-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="df62c-114">FILTERCHOOSE \_ \_ Agregar filtro</span><span class="sxs-lookup"><span data-stu-id="df62c-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="df62c-115">El parámetro *lParam* es un puntero a un búfer que aceptará una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable filtro.</span><span class="sxs-lookup"><span data-stu-id="df62c-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="df62c-116">La aplicación debe copiar la estructura de filtro que se va a agregar a este búfer.</span><span class="sxs-lookup"><span data-stu-id="df62c-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="df62c-117">\_comprobación de filtro de FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="df62c-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="df62c-118">El parámetro *lParam* es un puntero a una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable filtro.</span><span class="sxs-lookup"><span data-stu-id="df62c-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="df62c-119">FILTERCHOOSE \_ FILTERTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="df62c-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="df62c-120">El parámetro *lParam* es un puntero a un **valor DWORD** que aceptará una etiqueta de filtro de audio de forma de onda que se va a agregar al cuadro de lista desplegable de etiquetas de filtro.</span><span class="sxs-lookup"><span data-stu-id="df62c-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="df62c-121">FILTERCHOOSE \_ FILTERTAG \_ verify</span><span class="sxs-lookup"><span data-stu-id="df62c-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="df62c-122">El parámetro *lParam* es una etiqueta de filtro de audio de forma de onda que se mostrará en el cuadro de lista desplegable de etiquetas de filtro.</span><span class="sxs-lookup"><span data-stu-id="df62c-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="df62c-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="df62c-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="df62c-124">Valor definido por el cuadro de lista especificado en el parámetro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="df62c-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df62c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df62c-125">Return Value</span></span>

<span data-ttu-id="df62c-126">Devuelve **true** si una aplicación controla este mensaje o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="df62c-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df62c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df62c-127">Remarks</span></span>

<span data-ttu-id="df62c-128">Si la aplicación procesa la \_ \_ operación agregar filtro FILTERCHOOSE, el tamaño del búfer de memoria proporcionado en *lParam* se determinará a partir de la función [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="df62c-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="df62c-129">Si la aplicación procesa una operación de comprobación, la aplicación debe preceder al valor devuelto con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) para evitar que el cuadro de diálogo muestre esta selección o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) para permitir que el cuadro de diálogo muestre esta selección.</span><span class="sxs-lookup"><span data-stu-id="df62c-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="df62c-130">Si se procesa una operación de agregar, la aplicación debe preceder a la devolución con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) para indicar que no se requieren más adiciones o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) si se requieren más adiciones.</span><span class="sxs-lookup"><span data-stu-id="df62c-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="df62c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df62c-131">Requirements</span></span>



| <span data-ttu-id="df62c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="df62c-132">Requirement</span></span> | <span data-ttu-id="df62c-133">Value</span><span class="sxs-lookup"><span data-stu-id="df62c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df62c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df62c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="df62c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df62c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="df62c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df62c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="df62c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df62c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df62c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df62c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="df62c-139"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="df62c-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df62c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="df62c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df62c-141">Administrador de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="df62c-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="df62c-142">Mensajes de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="df62c-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





