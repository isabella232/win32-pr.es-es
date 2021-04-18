---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704563"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="0eb43-103">IAgentSpeechInputProperties::GetListeningTip</span><span class="sxs-lookup"><span data-stu-id="0eb43-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="0eb43-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0eb43-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="0eb43-105">Recupera un valor que indica si la sugerencia de escucha está habilitada para la presentación.</span><span class="sxs-lookup"><span data-stu-id="0eb43-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="0eb43-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0eb43-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0eb43-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span><span class="sxs-lookup"><span data-stu-id="0eb43-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="0eb43-108">Dirección de una variable que recibe **true** si la sugerencia de escucha está habilitada para la presentación o **false** si la sugerencia de escucha está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="0eb43-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="0eb43-109">Si [**GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**, la consulta de otras propiedades de entrada de voz devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="0eb43-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="0eb43-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0eb43-110">See Also</span></span>

[<span data-ttu-id="0eb43-111">**IAgentSpeechInputProperties::GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="0eb43-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




