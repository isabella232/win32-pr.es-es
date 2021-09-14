---
title: Convertir cadenas
description: Convertir cadenas
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- Función mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375206"
---
# <a name="converting-strings"></a>Convertir cadenas

Cuando se usa la función [**mciSendString,**](/previous-versions//dd757161(v=vs.85)) todos los valores pasados con el comando y todos los valores devueltos son cadenas de texto, por lo que la aplicación necesita rutinas de conversión para traducir de variables a cadenas o de nuevo. En el ejemplo siguiente se recupera el rectángulo de origen y se convierte la cadena devuelta en coordenadas de rectángulo.


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
> **Las estructuras RECT** se controlan de forma diferente en MCI que en otras partes de Windows; en MCI, el **miembro derecho** contiene el ancho del rectángulo y el **miembro** inferior contiene su alto. En la interfaz de cadena, se especifica un rectángulo *como X1,* *Y1,* *X2* e *Y2.* Las coordenadas *X1* e *Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *X2* e *Y2* especifican el ancho y el alto.

 

 

 