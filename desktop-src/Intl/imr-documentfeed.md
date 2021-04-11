---
description: Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con los parámetros establecidos como se muestra a continuación.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: Código de notificación de IMR_DOCUMENTFEED (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276728"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="d995f-104">Código de notificación de IMR \_ DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="d995f-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="d995f-105">Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d995f-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="d995f-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con los parámetros establecidos como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d995f-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="d995f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d995f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d995f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d995f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d995f-109">Establezca en IMR \_ DOCUMENTFEED.</span><span class="sxs-lookup"><span data-stu-id="d995f-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="d995f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d995f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d995f-111">Puntero a un búfer que va a contener la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="d995f-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d995f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d995f-112">Return Value</span></span>

<span data-ttu-id="d995f-113">Devuelve la estructura de la cadena de reconversión actual.</span><span class="sxs-lookup"><span data-stu-id="d995f-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="d995f-114">Si *lParam* se establece en **null**, la aplicación devuelve el tamaño necesario para que el búfer contenga la estructura.</span><span class="sxs-lookup"><span data-stu-id="d995f-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="d995f-115">El comando devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d995f-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d995f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d995f-116">Remarks</span></span>

<span data-ttu-id="d995f-117">El IME almacena en caché las cadenas convertidas para una mayor precisión de la conversión.</span><span class="sxs-lookup"><span data-stu-id="d995f-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="d995f-118">Una limitación del almacenamiento en caché del IME es que pierde la cadena convertida en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="d995f-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="d995f-119">La posición del símbolo de intercalación para la aplicación se mueve mediante una clave, por ejemplo, una tecla de cursor.</span><span class="sxs-lookup"><span data-stu-id="d995f-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="d995f-120">La posición del símbolo de intercalación para la aplicación se mueve por el mouse.</span><span class="sxs-lookup"><span data-stu-id="d995f-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="d995f-121">Se abre un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="d995f-121">A new document is opened.</span></span>

<span data-ttu-id="d995f-122">Con el comando **IMR \_ DOCUMENTFEED** , el IME puede actualizar las cadenas almacenadas en caché en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="d995f-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="d995f-123">El uso de este comando mejora la precisión de la conversión.</span><span class="sxs-lookup"><span data-stu-id="d995f-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="d995f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d995f-124">Requirements</span></span>



| <span data-ttu-id="d995f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d995f-125">Requirement</span></span> | <span data-ttu-id="d995f-126">Value</span><span class="sxs-lookup"><span data-stu-id="d995f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d995f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d995f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d995f-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d995f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d995f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d995f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d995f-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d995f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d995f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d995f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d995f-132"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d995f-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d995f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d995f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d995f-134">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d995f-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d995f-135">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d995f-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d995f-136">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="d995f-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="d995f-137">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d995f-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




