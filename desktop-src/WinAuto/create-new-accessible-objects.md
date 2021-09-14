---
title: Crear nuevos objetos accesibles
description: Crear nuevos objetos accesibles
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174925"
---
# <a name="create-new-accessible-objects"></a>Crear nuevos objetos accesibles

En este escenario, el servidor crea un nuevo objeto accesible en respuesta a cada [**solicitud OBJID \_ CLIENT.**](object-identifiers.md)

En el código de ejemplo siguiente, se recupera un puntero al control de los datos de ventana adicionales. Este y el identificador de ventana se pasan al constructor del objeto de servidor de accesibilidad personalizado (AccServer). Este objeto se crea cada vez [**que se recibe OBJID \_ CLIENT.**](object-identifiers.md)

Cuando se crea el objeto, el servidor obtiene una referencia, que se debe liberar después de llamar a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), para que el objeto se destruya en cuanto el cliente termine con él. Tenga en **cuenta que LresultFromObject** incrementa el recuento de referencias varias veces, pero es responsabilidad de las aplicaciones cliente y del entorno de ejecución Microsoft Active Accessibility liberar estas referencias.


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




