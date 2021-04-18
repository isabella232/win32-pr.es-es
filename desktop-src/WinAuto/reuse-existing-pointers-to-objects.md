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
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="3e160-103">Reutilizar punteros existentes a objetos</span><span class="sxs-lookup"><span data-stu-id="3e160-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="3e160-104">En este escenario, el servidor responde a una solicitud [**de \_ cliente de OBJID**](object-identifiers.md) mediante el mismo puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) cada vez.</span><span class="sxs-lookup"><span data-stu-id="3e160-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="3e160-105">En el código de ejemplo siguiente, el objeto de control se recupera de los datos de ventana adicionales y se llama a un método del control para recuperar el objeto de servidor de accesibilidad (la clase AccServer definida por la aplicación), si existe.</span><span class="sxs-lookup"><span data-stu-id="3e160-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="3e160-106">Si el servidor de accesibilidad todavía no existe, se crea.</span><span class="sxs-lookup"><span data-stu-id="3e160-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="3e160-107">Cuando se crea el objeto de servidor de accesibilidad, tiene un recuento de referencias de 1.</span><span class="sxs-lookup"><span data-stu-id="3e160-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="3e160-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa el recuento de referencias varias veces, pero estas referencias se liberarán cuando el cliente haya finalizado con el objeto.</span><span class="sxs-lookup"><span data-stu-id="3e160-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="3e160-109">El servidor libera su referencia cuando se destruye la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="3e160-109">The server releases its reference when the control window is destroyed.</span></span>


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



 

 




