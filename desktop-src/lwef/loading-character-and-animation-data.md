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
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="5b965-103">Cargar datos de animación y caracteres</span><span class="sxs-lookup"><span data-stu-id="5b965-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="5b965-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5b965-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5b965-105">Después de tener un puntero a la interfaz [**IAgentEx**](iagentex.md) , puede utilizar el método [**Load**](load-method.md) para cargar un carácter y recuperar su interfaz [**IAgentCharacterEx**](iagentcharacterex.md) .</span><span class="sxs-lookup"><span data-stu-id="5b965-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="5b965-106">Hay tres posibilidades diferentes para la ruta de acceso de carga de un carácter.</span><span class="sxs-lookup"><span data-stu-id="5b965-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="5b965-107">El primero es compatible con Microsoft Agent 1,5, donde la ruta de acceso especificada es la ruta de acceso completa y el nombre de archivo de un archivo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5b965-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="5b965-108">La segunda posibilidad es especificar solo el nombre de archivo, en cuyo caso el agente busca en el directorio chars.</span><span class="sxs-lookup"><span data-stu-id="5b965-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="5b965-109">La última posibilidad es proporcionar un parámetro Variant vacío que provoque que se cargue el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5b965-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


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



<span data-ttu-id="5b965-110">Puede utilizar esta interfaz para tener acceso a los métodos del carácter:</span><span class="sxs-lookup"><span data-stu-id="5b965-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="5b965-111">Cuando ya no necesite servicios del agente de Microsoft, como cuando se cierre la aplicación cliente, libere sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="5b965-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="5b965-112">Tenga en cuenta que al liberar la interfaz de caracteres no se descarga el carácter.</span><span class="sxs-lookup"><span data-stu-id="5b965-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="5b965-113">Llame al método [**Unload**](unload-method.md) para hacerlo antes de liberar la interfaz [**IAgentEx**](iagentex.md) :</span><span class="sxs-lookup"><span data-stu-id="5b965-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


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



 

 




