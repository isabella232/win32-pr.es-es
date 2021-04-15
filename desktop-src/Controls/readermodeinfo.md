---
title: Estructura READERMODEINFO
description: Contiene la información necesaria para inicializar la función DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO estructura de Windows (controles)
- PREADERMODEINFO controles de Windows de puntero de estructura
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491746"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="12fbd-105">Estructura READERMODEINFO</span><span class="sxs-lookup"><span data-stu-id="12fbd-105">READERMODEINFO structure</span></span>

<span data-ttu-id="12fbd-106">\[**READERMODEINFO** se admite a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="12fbd-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="12fbd-107">Es posible que no se admita en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="12fbd-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="12fbd-108">Contiene la información necesaria para inicializar la función [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="12fbd-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fbd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12fbd-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="12fbd-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="12fbd-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="12fbd-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="12fbd-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12fbd-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="12fbd-113">Required.</span></span> <span data-ttu-id="12fbd-114">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="12fbd-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="12fbd-115">Establezca este parámetro en **sizeof (READERMODE)** antes de llamar a [**DoReaderMode**](doreadermode.md).</span><span class="sxs-lookup"><span data-stu-id="12fbd-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="12fbd-116">**identificador**</span><span class="sxs-lookup"><span data-stu-id="12fbd-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-117">Tipo: **[ **hWnd**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12fbd-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="12fbd-118">Required.</span></span> <span data-ttu-id="12fbd-119">Identificador de la ventana que se va a usar para el modo de lectura.</span><span class="sxs-lookup"><span data-stu-id="12fbd-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="12fbd-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="12fbd-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-121">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12fbd-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-122">Marcas que personalizan la funcionalidad de la ventana de modo de lector.</span><span class="sxs-lookup"><span data-stu-id="12fbd-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="12fbd-123">Este parámetro puede ser 0; de lo contrario, uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="12fbd-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="12fbd-124">Value</span><span class="sxs-lookup"><span data-stu-id="12fbd-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="12fbd-125">Significado</span><span class="sxs-lookup"><span data-stu-id="12fbd-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="12fbd-126"><dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="12fbd-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="12fbd-127">Establece el cursor en el centro del área especificada en **PRC**.</span><span class="sxs-lookup"><span data-stu-id="12fbd-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="12fbd-128">Si no se especifica esta marca, la posición del cursor permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="12fbd-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="12fbd-129"><dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="12fbd-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="12fbd-130">Solo permite el desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="12fbd-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="12fbd-131"><dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="12fbd-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="12fbd-132">Solo permite el desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="12fbd-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="12fbd-133">**PRC**</span><span class="sxs-lookup"><span data-stu-id="12fbd-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-134">Tipo: **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="12fbd-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-135">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el área de desplazamiento en la ventana del modo lector.</span><span class="sxs-lookup"><span data-stu-id="12fbd-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="12fbd-136">Si este miembro es **null**, se utiliza la ventana completa como área de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="12fbd-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="12fbd-137">**pfnScroll**</span><span class="sxs-lookup"><span data-stu-id="12fbd-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-138">Tipo: **PFNREADERSCROLL**</span><span class="sxs-lookup"><span data-stu-id="12fbd-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-139">Un puntero a una función de devolución de llamada de [*ReaderScroll*](readerscroll.md) definida por la aplicación que se usa para notificar a la aplicación que la ventana debe desplazarse en una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="12fbd-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="12fbd-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="12fbd-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-141">Tipo: **PFNREADERTRANSLATEDISPATCH**</span><span class="sxs-lookup"><span data-stu-id="12fbd-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-142">Puntero a una función de devolución de llamada de [*TranslateDispatch*](translatedispatch.md) definida por la aplicación que se usa para obtener la primera notificación de los mensajes enviados a la ventana del modo de lectura.</span><span class="sxs-lookup"><span data-stu-id="12fbd-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="12fbd-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="12fbd-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="12fbd-144">Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12fbd-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="12fbd-145">Información adicional según sea necesario para la aplicación, leída por el autor de la llamada en la función de devolución de llamada [*ReaderScroll*](readerscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="12fbd-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12fbd-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12fbd-146">Remarks</span></span>

<span data-ttu-id="12fbd-147">Esta estructura no se declara en ningún encabezado público.</span><span class="sxs-lookup"><span data-stu-id="12fbd-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="12fbd-148">Para usarlo, debe incluir la declaración mostrada anteriormente en su propio encabezado.</span><span class="sxs-lookup"><span data-stu-id="12fbd-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fbd-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12fbd-149">Requirements</span></span>



| <span data-ttu-id="12fbd-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fbd-150">Requirement</span></span> | <span data-ttu-id="12fbd-151">Value</span><span class="sxs-lookup"><span data-stu-id="12fbd-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="12fbd-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12fbd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="12fbd-153">Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12fbd-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="12fbd-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12fbd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="12fbd-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="12fbd-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

