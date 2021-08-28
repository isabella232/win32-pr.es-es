---
title: Hacer referencia a máscaras en direcciones URL
description: Hacer referencia a máscaras en direcciones URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Reproductor de Windows Media máscaras,referencias URL
- máscaras, referencias url
- Referencias url en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a39a1dac1c4a20f563b58e1b8605c35527784867d81af60985b2e8e1d16c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934124"
---
# <a name="referencing-skins-in-urls"></a>Hacer referencia a máscaras en direcciones URL

Si usa una dirección URL para cargar un archivo multimedia que reproducirá Reproductor de Windows Media, puede solicitar que se use una máscara determinada con ese archivo. Si la máscara ya está instalada en la máquina del usuario, se usará. De lo contrario, se usará la máscara anterior.

Para solicitar una máscara, agregue lo siguiente al final de la dirección URL:


```C++
?WMPSkin=skinname
```



*skinname* es el nombre de la máscara que desea solicitar. No use comillas alrededor del nombre de la máscara.

Por ejemplo, para solicitar que se utilice la máscara de espacio en la cabeza, escriba la siguiente dirección URL HTTP:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> </dl>

 

 




