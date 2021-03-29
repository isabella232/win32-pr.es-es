---
title: Crear nuevas interfaces para el mismo objeto
description: Crear nuevas interfaces para el mismo objeto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665659"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Crear nuevas interfaces para el mismo objeto

En este escenario, el servidor responde a cada solicitud [**de \_ cliente de OBJID**](object-identifiers.md) obteniendo un nuevo puntero de interfaz al mismo objeto.

En el código de ejemplo siguiente, *m \_ pUIObj* es un puntero a un objeto que admite más de una interfaz del modelo de objetos componentes (com). Aunque se reutiliza un objeto existente, se crea un nuevo puntero de interfaz cada vez que se recupera el objeto, por lo que se debe reducir el recuento de referencias.


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




