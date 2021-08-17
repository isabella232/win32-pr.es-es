---
title: Creación de una File-Handler en un archivo DLL
description: Creación de una File-Handler en un archivo DLL
ms.assetid: 0cf7ef72-c675-4a67-97b3-18cccfb7ddc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0023de28f660473a1747ff05528ec5360674754b5c0bcd34f5ae3a28cc39412f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144758"
---
# <a name="creating-a-file-handler-instance-in-a-dll"></a>Creación de una File-Handler en un archivo DLL

Cuando una aplicación especifica el controlador de archivos DLL o el controlador de secuencias, el sistema lo busca en el Registro por su identificador de clase y lo carga. A continuación, el sistema [**llama a la función DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) del archivo DLL para crear una instancia del controlador de archivos o secuencias. En el ejemplo siguiente (escrito en C++) se muestra cómo un controlador de archivos crea una instancia de .


```C++
// Main DLL entry point. 
STDAPI DllGetClassObject(const CLSID FAR& rclsid, 
    const IID FAR& riid, void FAR* FAR* ppv) 
{ 
    HRESULT hresult; 
    hresult = CAVIFileCF::Create(rclsid, riid, ppv); 
    return hresult; 
} 
HRESULT CAVIFileCF::Create(const CLSID FAR&   rclsid, 
    const IID FAR& riid, void FAR* FAR*   ppv) 
{ 
// The following is the class factory creation and not an 
// actual PAVIFile. 
    CAVIFileCF FAR*   pAVIFileCF; 
    IUnknown FAR*   pUnknown; 
    HRESULT hresult; 
 
// Create the instance. 
    pAVIFileCF = new FAR CAVIFileCF(rclsid, &pUnknown); 
    if (pAVIFileCF == NULL) 
        return ResultFromScode(E_OUTOFMEMORY); 
 
// Set the interface pointer. 
    hresult = pUnknown->QueryInterface(riid, ppv); 
    if (FAILED(GetScode(hresult))) 
        delete pAVIFileCF; 
    return hresult; 
} 

```



 

 