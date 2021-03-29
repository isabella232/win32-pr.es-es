---
title: Convertir cadenas
description: Convertir cadenas
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995126"
---
# <a name="converting-strings"></a><span data-ttu-id="0f055-104">Convertir cadenas</span><span class="sxs-lookup"><span data-stu-id="0f055-104">Converting Strings</span></span>

<span data-ttu-id="0f055-105">Cuando se usa la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , todos los valores que se pasan con el comando y todos los valores devueltos son cadenas de texto, por lo que la aplicación necesita rutinas de conversión para convertir variables a cadenas o viceversa.</span><span class="sxs-lookup"><span data-stu-id="0f055-105">When you use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, all values passed with the command and all return values are text strings, so your application needs conversion routines to translate from variables to strings or back again.</span></span> <span data-ttu-id="0f055-106">En el ejemplo siguiente se recupera el rectángulo de origen y se convierte la cadena devuelta en coordenadas del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0f055-106">The following example retrieves the source rectangle and converts the returned string into rectangle coordinates.</span></span>


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> <span data-ttu-id="0f055-107">Las estructuras **Rect** se administran de forma diferente en MCI que en otras partes de Windows. en MCI, el miembro de la **derecha** contiene el ancho del rectángulo y el miembro **inferior** contiene su alto.</span><span class="sxs-lookup"><span data-stu-id="0f055-107">**RECT** structures are handled differently in MCI than in other parts of Windows; in MCI, the **right** member contains the width of the rectangle and the **bottom** member contains its height.</span></span> <span data-ttu-id="0f055-108">En la interfaz de cadena, se especifica un rectángulo como *x1*, *Y1*, *x2* e *Y2*.</span><span class="sxs-lookup"><span data-stu-id="0f055-108">In the string interface, a rectangle is specified as *X1*, *Y1*, *X2*, and *Y2*.</span></span> <span data-ttu-id="0f055-109">Las coordenadas *x1* e *Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2* e *Y2* especifican el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="0f055-109">The coordinates *X1* and *Y1* specify the upper-left corner of the rectangle, and the coordinates *X2* and *Y2* specify the width and height.</span></span>

 

 

 