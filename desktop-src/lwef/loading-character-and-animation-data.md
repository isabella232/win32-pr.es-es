---
title: Cargar datos de caracteres y animaciones
description: Cargar datos de caracteres y animaciones
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961435"
---
# <a name="loading-character-and-animation-data"></a>Cargar datos de caracteres y animaciones

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Después de tener un puntero a la [**interfaz IAgentEx,**](iagentex.md) puede usar el método [**Load**](load-method.md) para cargar un carácter y recuperar su [**interfaz IAgentCharacterEx.**](iagentcharacterex.md) Hay tres posibilidades diferentes para la ruta de acceso de carga de un carácter. La primera es compatible con Microsoft Agent 1.5, donde la ruta de acceso especificada es la ruta de acceso completa y el nombre de archivo de un archivo de caracteres. La segunda posibilidad es especificar solo el nombre de archivo, en cuyo caso, el Agente busca en su directorio Chars. La última posibilidad es proporcionar un parámetro Variant vacío que hace que se cargue el carácter predeterminado.


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



Puede usar esta interfaz para acceder a los métodos del carácter:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Cuando ya no necesite servicios de Microsoft Agent, como cuando se cierre la aplicación cliente, libere sus interfaces. Tenga en cuenta que liberar la interfaz de caracteres no descarga el carácter. Llame al [**método Unload**](unload-method.md) para hacerlo antes de liberar la [**interfaz IAgentEx:**](iagentex.md)


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




