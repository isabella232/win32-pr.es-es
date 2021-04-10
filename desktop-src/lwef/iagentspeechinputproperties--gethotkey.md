---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074987"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="24770-103">IAgentSpeechInputProperties::GetHotKey</span><span class="sxs-lookup"><span data-stu-id="24770-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="24770-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24770-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="24770-105">Recupera la asignación de teclado actual para la clave de escucha de entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="24770-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="24770-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="24770-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="24770-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span><span class="sxs-lookup"><span data-stu-id="24770-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="24770-108">Dirección de un BSTR que recibe la configuración de Hotkey actual usada para abrir el canal de audio para la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="24770-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="24770-109">Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**, al consultar esta configuración se produce un error.</span><span class="sxs-lookup"><span data-stu-id="24770-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="24770-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="24770-110">See Also</span></span>

[<span data-ttu-id="24770-111">**IAgentSpeechInputProperties::GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="24770-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




