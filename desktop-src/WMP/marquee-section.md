---
title: Sección Marquee
description: Sección Marquee
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Reproductor de Windows Media Máscaras móviles, marques
- máscaras, marques
- crear máscaras, sección Marquee
- escribir código para máscaras, sección Marquee
- marquees en máscaras, sección Marquee
- archivos de definición de máscara, sección Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ddb53edd3f1efbbcbc5491604fd4022673b1234038770fcf44cd29ef4f3aca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123454"
---
# <a name="marquee-section"></a>Sección Marquee

La sección Marquee contiene información sobre el cuadro de texto marquesina, que mostrará texto de desplazamiento:


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Se mostrará el título y el autor del elemento multimedia actual, aunque puede mostrar cualquier tipo de texto en la marquesina. Por ejemplo, también puede incluir Filename, Status y Playlist en la marquesina.

> [!Note]  
> Para mantener la compatibilidad con las versiones de Reproductor de Windows Media Mobile anteriores a Reproductor de Windows Media 10 Mobile, el uso de "Tiempo" en un archivo de definición de máscara todavía se considera válido.

 

Para obtener más información sobre la sección Marquee, vea Marquee in the Skin Reference [(Marquee](marquee.md) en la referencia de máscara).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




