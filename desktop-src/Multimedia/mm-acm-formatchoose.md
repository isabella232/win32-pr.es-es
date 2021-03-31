---
title: Mensaje de MM_ACM_FORMATCHOOSE (MSACM. h)
description: El \_ mensaje FORMATCHOOSE de mm ACM \_ notifica a una función de enlace del cuadro de diálogo acmFormatChoose antes de agregar un elemento a uno de los tres cuadros de lista desplegable.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- Mensaje de MM_ACM_FORMATCHOOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804093"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="a6fda-104">\_ \_ Mensaje FORMATCHOOSE de mm ACM</span><span class="sxs-lookup"><span data-stu-id="a6fda-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="a6fda-105">El **mensaje \_ \_ FORMATCHOOSE de mm ACM** notifica a una función de enlace del cuadro de diálogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) antes de agregar un elemento a uno de los tres cuadros de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="a6fda-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="a6fda-106">Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6fda-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="a6fda-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6fda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fda-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="a6fda-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="a6fda-109">Cuadro de lista desplegable que se va a inicializar y una operación de comprobación o adición.</span><span class="sxs-lookup"><span data-stu-id="a6fda-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="a6fda-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fda-110">Requirement</span></span> | <span data-ttu-id="a6fda-111">Value</span><span class="sxs-lookup"><span data-stu-id="a6fda-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fda-112">\_comprobación personalizada de FORMATCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="a6fda-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="a6fda-113">El parámetro *lParam* es un puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable Nombre personalizado.</span><span class="sxs-lookup"><span data-stu-id="a6fda-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="a6fda-114">\_Agregar formato \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="a6fda-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="a6fda-115">El parámetro *lParam* es un puntero a un búfer que aceptará una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable formato.</span><span class="sxs-lookup"><span data-stu-id="a6fda-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="a6fda-116">La aplicación debe copiar la estructura de formato que se va a agregar a este búfer.</span><span class="sxs-lookup"><span data-stu-id="a6fda-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="a6fda-117">\_comprobación de formato de FORMATCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="a6fda-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="a6fda-118">El parámetro *lParam* es un puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable formato.</span><span class="sxs-lookup"><span data-stu-id="a6fda-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="a6fda-119">FORMATCHOOSE \_ FORMATTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="a6fda-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="a6fda-120">El parámetro *lParam* es un puntero a una variable que aceptará una etiqueta de formato de audio de forma de onda que se va a agregar al cuadro de lista desplegable de etiqueta de formato.</span><span class="sxs-lookup"><span data-stu-id="a6fda-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="a6fda-121">FORMATCHOOSE \_ FORMATTAG \_ verify</span><span class="sxs-lookup"><span data-stu-id="a6fda-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="a6fda-122">El parámetro *lParam* es una etiqueta de formato de audio de forma de onda que se mostrará en el cuadro de lista desplegable formato de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a6fda-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="a6fda-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="a6fda-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="a6fda-124">Valor definido por el cuadro de lista especificado en el parámetro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="a6fda-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fda-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6fda-125">Return Value</span></span>

<span data-ttu-id="a6fda-126">Devuelve **true** si una aplicación controla este mensaje o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a6fda-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6fda-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6fda-127">Remarks</span></span>

<span data-ttu-id="a6fda-128">Si la aplicación procesa la \_ operación de \_ Agregar formato FILTERCHOOSE, el tamaño del búfer de memoria proporcionado en *lParam* se determinará a partir de la función [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="a6fda-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="a6fda-129">Si la aplicación está procesando una operación de comprobación, puede impedir que el cuadro de diálogo muestre esta selección mediante una llamada a la función **SetWindowLong** con *NINDEX* establecida en DWL \_ MSGRESULT y *lNewLong* establecida en **false** (convertir a un tipo de datos **Long** ).</span><span class="sxs-lookup"><span data-stu-id="a6fda-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="a6fda-130">Para permitir que el cuadro de diálogo muestre esta selección, llame a esta función con *lNewLong* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="a6fda-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="a6fda-131">Si la aplicación está procesando una operación de agregar, puede indicar que no se requieren más adiciones mediante una llamada a la función **SetWindowLong** con *NINDEX* establecida en DWL \_ MSGRESULT y *lNewLong* establecida en **false** (convertir a un tipo de datos **Long** ).</span><span class="sxs-lookup"><span data-stu-id="a6fda-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="a6fda-132">Para indicar que se necesitan más adiciones, llame a esta función con *lNewLong* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="a6fda-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6fda-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6fda-133">Requirements</span></span>



| <span data-ttu-id="a6fda-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fda-134">Requirement</span></span> | <span data-ttu-id="a6fda-135">Value</span><span class="sxs-lookup"><span data-stu-id="a6fda-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fda-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6fda-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6fda-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a6fda-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a6fda-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6fda-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6fda-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6fda-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6fda-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6fda-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6fda-141"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6fda-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6fda-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6fda-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fda-143">Administrador de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="a6fda-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a6fda-144">Mensajes de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="a6fda-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

