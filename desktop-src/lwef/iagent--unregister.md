---
title: IAgent anular registro
description: IAgent anular registro
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904598"
---
# <a name="iagentunregister"></a><span data-ttu-id="80e94-103">IAgent:: unregister</span><span class="sxs-lookup"><span data-stu-id="80e94-103">IAgent::Unregister</span></span>

<span data-ttu-id="80e94-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80e94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="80e94-105">Descarga los datos de caracteres para el carácter especificado de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="80e94-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="80e94-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="80e94-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="80e94-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span><span class="sxs-lookup"><span data-stu-id="80e94-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="80e94-108">IDENTIFICADOR del receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="80e94-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="80e94-109">Utilice este método cuando ya no necesite servicios del agente de Microsoft, como cuando se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80e94-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="80e94-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80e94-110">See Also</span></span>

[<span data-ttu-id="80e94-111">**IAgent:: Register**</span><span class="sxs-lookup"><span data-stu-id="80e94-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 