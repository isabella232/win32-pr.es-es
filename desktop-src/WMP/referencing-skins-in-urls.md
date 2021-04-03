---
title: Referencia a máscaras en direcciones URL
description: Referencia a máscaras en direcciones URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Máscaras de Windows Media Player, referencias de URL
- máscaras, referencias de URL
- Referencias a direcciones URL en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779584"
---
# <a name="referencing-skins-in-urls"></a>Referencia a máscaras en direcciones URL

Si usa una dirección URL para cargar un archivo multimedia que reproducirá Windows Media Player, puede solicitar que se use una máscara determinada con ese archivo. Si la máscara ya está instalada en el equipo del usuario, se utilizará; de lo contrario, se usará la máscara anterior.

Para solicitar una máscara, agregue lo siguiente al final de la dirección URL:


```C++
?WMPSkin=skinname
```



*skinName* es el nombre de la máscara que desea solicitar. No use comillas alrededor del nombre de la máscara.

Por ejemplo, para solicitar que se use la máscara headspace, escriba la siguiente dirección URL http:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> </dl>

 

 




