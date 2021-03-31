---
title: Cómo usar operaciones de edición de texto enriquecidas
description: Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit. Puede recuperar el texto seleccionado o un intervalo de texto especificado.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995676"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="53322-104">Cómo usar operaciones de edición de texto enriquecidas</span><span class="sxs-lookup"><span data-stu-id="53322-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="53322-105">Una aplicación puede enviar mensajes para recuperar o buscar texto en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="53322-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="53322-106">Puede recuperar el texto seleccionado o un intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="53322-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="53322-107">Para obtener el texto seleccionado en un control Rich Edit, utilice el [**mensaje \_ GETSELTEXT em**](em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="53322-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="53322-108">El texto se copia en la matriz de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="53322-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="53322-109">Debe asegurarse de que la matriz es lo suficientemente grande como para contener el texto seleccionado más un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="53322-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="53322-110">Para recuperar un intervalo de texto especificado, use el [**mensaje \_ GETTEXTRANGE em**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="53322-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="53322-111">La estructura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) utilizada con este mensaje especifica el intervalo de texto que se va a recuperar y apunta a una matriz de caracteres que recibe el texto.</span><span class="sxs-lookup"><span data-stu-id="53322-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="53322-112">En este caso, la aplicación debe asegurarse de que la matriz es lo suficientemente grande como para el texto especificado y un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="53322-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="53322-113">Puede buscar una cadena en un control Rich Edit mediante los mensajes [**em \_ Textobuscado**](em-findtext.md) o [**em \_ FINDTEXTEX**](em-findtextex.md) , o sus equivalentes de Unicode, [**em \_ FINDTEXTW**](em-findtextw.md) y [**em \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="53322-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="53322-114">La estructura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que se usa con las versiones no extendidas especifica el intervalo de texto que se va a buscar y la cadena que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="53322-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="53322-115">Las versiones extendidas usan una estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , que especifica la misma información y también recibe los puntos inicial y final del intervalo de caracteres del texto encontrado.</span><span class="sxs-lookup"><span data-stu-id="53322-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="53322-116">También puede especificar estas opciones como si la búsqueda distinga mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="53322-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="53322-117">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="53322-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="53322-118">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="53322-118">Technologies</span></span>

-   [<span data-ttu-id="53322-119">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="53322-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="53322-120">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53322-120">Prerequisites</span></span>

-   <span data-ttu-id="53322-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="53322-121">C/C++</span></span>
-   <span data-ttu-id="53322-122">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="53322-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="53322-123">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="53322-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="53322-124">Usar una operación de edición de texto enriquecida</span><span class="sxs-lookup"><span data-stu-id="53322-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="53322-125">En la función de ejemplo siguiente se busca el texto especificado en el texto seleccionado en un control Rich Edit que admita Unicode.</span><span class="sxs-lookup"><span data-stu-id="53322-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="53322-126">Si se encuentra el destino, se convierte en la nueva selección.</span><span class="sxs-lookup"><span data-stu-id="53322-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="53322-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53322-127">Remarks</span></span>

<span data-ttu-id="53322-128">Microsoft Rich Edit 3,0 también es compatible con la función del editor de métodos de entrada (IME) HexToUnicode, que permite a un usuario convertir entre hexadecimales y Unicode mediante el uso de teclas de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="53322-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="53322-129">Para obtener más información, consulte [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="53322-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53322-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53322-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53322-131">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="53322-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="53322-132">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="53322-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 