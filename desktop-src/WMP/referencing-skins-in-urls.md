---
title: Hacer referencia a máscaras en direcciones URL
description: Hacer referencia a máscaras en direcciones URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Reproductor de Windows Media máscaras,referencias url
- skins,URL references
- Referencias url en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581333"
---
# <a name="referencing-skins-in-urls"></a>Hacer referencia a máscaras en direcciones URL

Si usa una dirección URL para cargar un archivo multimedia que reproducirá Reproductor de Windows Media, puede solicitar que se use una máscara determinada con ese archivo. Si la máscara ya está instalada en el equipo del usuario, se usará. De lo contrario, se usará la máscara anterior.

Para solicitar una máscara, agregue lo siguiente al final de la dirección URL:


```C++
?WMPSkin=skinname
```



*skinname* es el nombre de la máscara que desea solicitar. No use comillas alrededor del nombre de la máscara.

Por ejemplo, para solicitar que se utilice la máscara de espacio en la cabeza, escriba la siguiente dirección URL http:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las máscaras**](about-skins.md)
</dt> </dl>

 

 




