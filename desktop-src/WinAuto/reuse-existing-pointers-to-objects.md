---
title: Reutilizar punteros existentes a objetos
description: Reutilizar punteros existentes a objetos
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704590"
---
# <a name="reuse-existing-pointers-to-objects"></a>Reutilizar punteros existentes a objetos

En este escenario, el servidor responde a una solicitud [**de \_ cliente de OBJID**](object-identifiers.md) mediante el mismo puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) cada vez.

En el código de ejemplo siguiente, el objeto de control se recupera de los datos de ventana adicionales y se llama a un método del control para recuperar el objeto de servidor de accesibilidad (la clase AccServer definida por la aplicación), si existe. Si el servidor de accesibilidad todavía no existe, se crea.

Cuando se crea el objeto de servidor de accesibilidad, tiene un recuento de referencias de 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa el recuento de referencias varias veces, pero estas referencias se liberarán cuando el cliente haya finalizado con el objeto. El servidor libera su referencia cuando se destruye la ventana de control.


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




