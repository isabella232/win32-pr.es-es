---
description: Se envía a la ventana más afectada después de cambiar el idioma de entrada de una aplicación. Debe realizar cualquier configuración específica de la aplicación y pasar el mensaje a la función DefWindowProc, que pasa el mensaje a todas las ventanas secundarias de primer nivel.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332410"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="1670b-104">Mensaje \_ INPUTLANGCHANGE de WM</span><span class="sxs-lookup"><span data-stu-id="1670b-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="1670b-105">Se envía a la ventana más afectada después de cambiar el idioma de entrada de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1670b-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="1670b-106">Debe realizar cualquier configuración específica de la aplicación y pasar el mensaje a la función [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que pasa el mensaje a todas las ventanas secundarias de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="1670b-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="1670b-107">Estas ventanas secundarias pueden pasar el mensaje [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que pase el mensaje a sus ventanas secundarias, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="1670b-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="1670b-108">Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1670b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="1670b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1670b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1670b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1670b-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="1670b-111">Tipo: **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1670b-111">Type: **WPARAM**</span></span>

<span data-ttu-id="1670b-112">Página [de códigos](../Intl/code-pages.md) de la nueva configuración regional.</span><span class="sxs-lookup"><span data-stu-id="1670b-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="1670b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1670b-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="1670b-114">Tipo: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="1670b-114">Type: **LPARAM**</span></span>

<span data-ttu-id="1670b-115">Identificador de configuración regional de entrada **HKL.**</span><span class="sxs-lookup"><span data-stu-id="1670b-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="1670b-116">Para obtener más información, [vea Idiomas, configuraciones regionales y diseños de teclado.](../inputdev/about-keyboard-input.md)</span><span class="sxs-lookup"><span data-stu-id="1670b-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1670b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1670b-117">Return value</span></span>

<span data-ttu-id="1670b-118">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1670b-118">Type: **LRESULT**</span></span>

<span data-ttu-id="1670b-119">Una aplicación debe devolver un valor distinto de cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1670b-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1670b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1670b-120">Remarks</span></span>

<span data-ttu-id="1670b-121">Puede recuperar el nombre de [la configuración regional del teclado](../Intl/locale-names.md) mediante la función [LCIDToLocaleName.](/windows/win32/api/winnls/nf-winnls-lcidtolocalename)</span><span class="sxs-lookup"><span data-stu-id="1670b-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="1670b-122">Con el nombre de configuración regional puede usar funciones [de configuración regional modernas:](/windows/win32/intl/calling-the--locale-name--functions)</span><span class="sxs-lookup"><span data-stu-id="1670b-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="1670b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1670b-123">Requirements</span></span>

| <span data-ttu-id="1670b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1670b-124">Requirement</span></span> | <span data-ttu-id="1670b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1670b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1670b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1670b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1670b-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1670b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1670b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1670b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1670b-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1670b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1670b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1670b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1670b-131"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1670b-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="1670b-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1670b-132">See also</span></span>

<span data-ttu-id="1670b-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1670b-133">**Reference**</span></span>

- [<span data-ttu-id="1670b-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1670b-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="1670b-135">**WM \_ INPUTLANGCHANGEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="1670b-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="1670b-136">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="1670b-136">**Conceptual**</span></span>

- [<span data-ttu-id="1670b-137">Windows</span><span class="sxs-lookup"><span data-stu-id="1670b-137">Windows</span></span>](windows.md) 
