---
title: Crear nuevas interfaces para el mismo objeto
description: Crear nuevas interfaces para el mismo objeto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae1d6328b6d803e4d20207381fe596c5f584fee8281e1e6651ffc2325fb044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998715"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Crear nuevas interfaces para el mismo objeto

En este escenario, el servidor responde a cada solicitud [**OBJID \_ CLIENT**](object-identifiers.md) mediante la obtención de un nuevo puntero de interfaz al mismo objeto.

En el código de ejemplo siguiente, *m \_ pUIObj* es un puntero a un objeto que admite más de una interfaz de Modelo de objetos componentes (COM). Aunque se reutiliza un objeto existente, se crea un nuevo puntero de interfaz cada vez que se recupera el objeto, por lo que se debe disminuir el recuento de referencias.


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



 

 




