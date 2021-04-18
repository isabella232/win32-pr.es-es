---
title: comando UPDATE
description: El comando UPDATE vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- comando actualizar Windows multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535349"
---
# <a name="update-command"></a><span data-ttu-id="8d319-105">comando UPDATE</span><span class="sxs-lookup"><span data-stu-id="8d319-105">update command</span></span>

<span data-ttu-id="8d319-106">El comando UPDATE vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado.</span><span class="sxs-lookup"><span data-stu-id="8d319-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="8d319-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="8d319-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8d319-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8d319-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8d319-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d319-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8d319-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8d319-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8d319-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8d319-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d319-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8d319-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span><span class="sxs-lookup"><span data-stu-id="8d319-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="8d319-114">Identificador de un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="8d319-114">Handle of a DC.</span></span> <span data-ttu-id="8d319-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Update** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="8d319-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="8d319-116">Value</span><span class="sxs-lookup"><span data-stu-id="8d319-116">Value</span></span>        | <span data-ttu-id="8d319-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8d319-117">Meaning</span></span>                       | <span data-ttu-id="8d319-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8d319-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="8d319-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="8d319-119">digitalvideo</span></span> | <span data-ttu-id="8d319-120">HDC *HDC* HDC *HDC* en *Rect*</span><span class="sxs-lookup"><span data-stu-id="8d319-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="8d319-121">pintar HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="8d319-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="8d319-122">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszHDC** y su significado.</span><span class="sxs-lookup"><span data-stu-id="8d319-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="8d319-123">Value</span><span class="sxs-lookup"><span data-stu-id="8d319-123">Value</span></span>               | <span data-ttu-id="8d319-124">Significado</span><span class="sxs-lookup"><span data-stu-id="8d319-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d319-125">HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="8d319-125">hdc *hdc*</span></span>           | <span data-ttu-id="8d319-126">Especifica el identificador del controlador de dominio que se va a pintar.</span><span class="sxs-lookup"><span data-stu-id="8d319-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="8d319-127">HDC *HDC* en *Rect*</span><span class="sxs-lookup"><span data-stu-id="8d319-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="8d319-128">Especifica el rectángulo de recorte relativo al rectángulo de cliente.</span><span class="sxs-lookup"><span data-stu-id="8d319-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="8d319-129">pintar HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="8d319-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="8d319-130">Pinta el controlador de dominio cuando la aplicación recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) diseñado para un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="8d319-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="8d319-131">Para especificar el identificador del controlador de dominio, use la cadena "HDC" seguida de una representación ASCII del identificador.</span><span class="sxs-lookup"><span data-stu-id="8d319-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="8d319-132">El rectángulo se especifica como **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="8d319-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="8d319-133">Las coordenadas **x1 Y1** especifican la esquina superior izquierda del rectángulo y las coordenadas **x2 Y2** especifican el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="8d319-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="8d319-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8d319-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8d319-135">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="8d319-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="8d319-136">En el caso de los dispositivos de vídeo digital, también se puede especificar "Test".</span><span class="sxs-lookup"><span data-stu-id="8d319-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="8d319-137">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8d319-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d319-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d319-138">Return Value</span></span>

<span data-ttu-id="8d319-139">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8d319-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="8d319-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d319-140">Examples</span></span>

<span data-ttu-id="8d319-141">El comando siguiente actualiza la ventana de presentación completa utilizada por el dispositivo "Movie".</span><span class="sxs-lookup"><span data-stu-id="8d319-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="8d319-142">El número 203 es un identificador de un controlador de dominio Obtenido de la función [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="8d319-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="8d319-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d319-143">Requirements</span></span>



| <span data-ttu-id="8d319-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d319-144">Requirement</span></span> | <span data-ttu-id="8d319-145">Value</span><span class="sxs-lookup"><span data-stu-id="8d319-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8d319-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d319-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8d319-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d319-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d319-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d319-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8d319-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d319-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8d319-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d319-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d319-151">MCI</span><span class="sxs-lookup"><span data-stu-id="8d319-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8d319-152">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="8d319-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

