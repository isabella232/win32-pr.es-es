---
title: Crear nuevos objetos accesibles
description: Crear nuevos objetos accesibles
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776627"
---
# <a name="create-new-accessible-objects"></a>Crear nuevos objetos accesibles

En este escenario, el servidor crea un nuevo objeto accesible en respuesta a cada solicitud de [**\_ cliente de OBJID**](object-identifiers.md) .

En el código de ejemplo siguiente, se recupera un puntero al control de los datos de ventana adicionales. Este y el identificador de ventana se pasan al constructor del objeto del servidor de accesibilidad personalizado (AccServer). Este objeto se crea cuando se recibe el [**\_ cliente de OBJID**](object-identifiers.md) .

Cuando se crea el objeto, el servidor obtiene una referencia, que se debe liberar después de llamar a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), para que el objeto se destruya tan pronto como el cliente termine de usarlo. Tenga en cuenta que **LresultFromObject** incrementa el recuento de referencias varias veces, pero es responsabilidad de las aplicaciones cliente y del tiempo de ejecución de Microsoft Active Accessibility para liberar estas referencias.


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



 

 




