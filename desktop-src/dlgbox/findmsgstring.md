---
title: Mensaje FINDMSGSTRING (commdlg. h)
description: Un cuadro de diálogo Buscar o reemplazar envía el mensaje registrado FINDMSGSTRING al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón Buscar siguiente, reemplazar o reemplazar todo, o cierra el cuadro de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Cuadros de diálogo de mensaje de FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535260"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="956a0-104">Mensaje FINDMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="956a0-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="956a0-105">Un cuadro de diálogo **Buscar** o **reemplazar** envía el mensaje registrado **FINDMSGSTRING** al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón **Buscar siguiente**, **reemplazar** o **reemplazar todo** , o cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="956a0-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="956a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="956a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="956a0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956a0-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="956a0-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="956a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="956a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956a0-110">Puntero a una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .</span><span class="sxs-lookup"><span data-stu-id="956a0-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="956a0-111">Los miembros de esta estructura contienen la entrada más reciente del usuario, incluida la cadena que se va a buscar, la cadena de reemplazo (si existe) y las opciones de búsqueda y reemplazo.</span><span class="sxs-lookup"><span data-stu-id="956a0-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956a0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="956a0-112">Return value</span></span>

<span data-ttu-id="956a0-113">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="956a0-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="956a0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="956a0-114">Remarks</span></span>

<span data-ttu-id="956a0-115">Debe especificar la constante **FINDMSGSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="956a0-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="956a0-116">Al crear el cuadro de diálogo, use el miembro **hwndOwner** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar la ventana que recibirá mensajes **FINDMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="956a0-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="956a0-117">El miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) incluye una de las marcas siguientes para indicar el evento que provocó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="956a0-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="956a0-118">Marca</span><span class="sxs-lookup"><span data-stu-id="956a0-118">Flag</span></span>                            | <span data-ttu-id="956a0-119">Significado</span><span class="sxs-lookup"><span data-stu-id="956a0-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956a0-120">**Fr \_ DIALOGTERM** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="956a0-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="956a0-121">El cuadro de diálogo se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="956a0-121">The dialog box is closing.</span></span> <span data-ttu-id="956a0-122">Una vez que la ventana propietaria procesa este mensaje, el identificador del cuadro de diálogo ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="956a0-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="956a0-123">**Fr \_ FINDNEXT** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="956a0-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="956a0-124">El usuario hizo clic en el botón **Buscar siguiente** en un cuadro de diálogo **Buscar** o **reemplazar** .</span><span class="sxs-lookup"><span data-stu-id="956a0-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="956a0-125">El miembro **lpstrFindWhat** especifica la cadena que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="956a0-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="956a0-126">**Fr \_ REEMPLAZAR** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="956a0-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="956a0-127">El usuario hizo clic en el botón **reemplazar** en un cuadro de diálogo **reemplazar** .</span><span class="sxs-lookup"><span data-stu-id="956a0-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="956a0-128">El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="956a0-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="956a0-129">**Fr \_ REPLACEALL** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="956a0-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="956a0-130">El usuario hizo clic en el botón **reemplazar todo** en un cuadro de diálogo **reemplazar** .</span><span class="sxs-lookup"><span data-stu-id="956a0-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="956a0-131">El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="956a0-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="956a0-132">En el caso de los mensajes **Buscar siguiente** o **reemplazar todo** , el miembro de **marcas** puede incluir una o varias de las marcas siguientes para indicar las opciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="956a0-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="956a0-133">Marca</span><span class="sxs-lookup"><span data-stu-id="956a0-133">Flag</span></span>                           | <span data-ttu-id="956a0-134">Significado</span><span class="sxs-lookup"><span data-stu-id="956a0-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956a0-135">**Fr \_ DOWN** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="956a0-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="956a0-136">Si se establece, se selecciona el botón **abajo** de los botones de radio dirección que indica que el usuario desea buscar desde la ubicación actual hasta el final del documento.</span><span class="sxs-lookup"><span data-stu-id="956a0-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="956a0-137">Si no se establece el valor de **fr \_ Down** , se selecciona el botón **subir** para que el usuario desee buscar en el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="956a0-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="956a0-138">**Fr \_ MATCHCASE** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="956a0-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="956a0-139">Si se establece, la casilla **Coincidir mayúsculas y minúsculas** está activada, lo que indica que el usuario desea que la búsqueda distinga entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="956a0-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="956a0-140">Si no se establece **fr \_ MATCHCASE** , la casilla está desactivada, por lo que la búsqueda no debe distinguir mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="956a0-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="956a0-141">**Fr \_ WHOLEWORD** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="956a0-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="956a0-142">Si se establece, la casilla **coincidir solo con palabras completas** está activada, lo que indica que el usuario desea buscar únicamente palabras completas que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="956a0-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="956a0-143">Si no se establece **fr \_ WHOLEWORD** , la casilla está desactivada, por lo que también debe buscar fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="956a0-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="956a0-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="956a0-144">Requirements</span></span>



| <span data-ttu-id="956a0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="956a0-145">Requirement</span></span> | <span data-ttu-id="956a0-146">Value</span><span class="sxs-lookup"><span data-stu-id="956a0-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956a0-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956a0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="956a0-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="956a0-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="956a0-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956a0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="956a0-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="956a0-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="956a0-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="956a0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="956a0-152"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="956a0-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="956a0-153">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="956a0-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="956a0-154">**FINDMSGSTRINGW** (Unicode) y **FINDMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="956a0-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="956a0-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="956a0-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="956a0-156">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="956a0-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="956a0-157">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="956a0-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="956a0-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="956a0-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="956a0-159">**Vista**</span><span class="sxs-lookup"><span data-stu-id="956a0-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="956a0-160">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="956a0-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

