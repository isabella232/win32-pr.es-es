---
title: Cargar datos de animación y caracteres
description: Cargar datos de animación y caracteres
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704739"
---
# <a name="loading-character-and-animation-data"></a>Cargar datos de animación y caracteres

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Después de tener un puntero a la interfaz [**IAgentEx**](iagentex.md) , puede utilizar el método [**Load**](load-method.md) para cargar un carácter y recuperar su interfaz [**IAgentCharacterEx**](iagentcharacterex.md) . Hay tres posibilidades diferentes para la ruta de acceso de carga de un carácter. El primero es compatible con Microsoft Agent 1,5, donde la ruta de acceso especificada es la ruta de acceso completa y el nombre de archivo de un archivo de caracteres. La segunda posibilidad es especificar solo el nombre de archivo, en cuyo caso el agente busca en el directorio chars. La última posibilidad es proporcionar un parámetro Variant vacío que provoque que se cargue el carácter predeterminado.


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



Puede utilizar esta interfaz para tener acceso a los métodos del carácter:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Cuando ya no necesite servicios del agente de Microsoft, como cuando se cierre la aplicación cliente, libere sus interfaces. Tenga en cuenta que al liberar la interfaz de caracteres no se descarga el carácter. Llame al método [**Unload**](unload-method.md) para hacerlo antes de liberar la interfaz [**IAgentEx**](iagentex.md) :


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



 

 




