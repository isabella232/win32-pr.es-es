---
title: Sección marquesina
description: Sección marquesina
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- crear máscaras, sección marquesina
- escribir código para máscaras, sección marquesina
- marquesinas en máscaras, sección de marquesina
- archivos de definición de máscara, sección de marquesina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780053"
---
# <a name="marquee-section"></a>Sección marquesina

La sección marquesina contiene información sobre el cuadro de texto marquesina, que mostrará el texto desplazado:


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Esto mostrará el título y el autor del elemento multimedia actual, aunque puede mostrar cualquier tipo de texto en la marquesina. Por ejemplo, también puede incluir el nombre de archivo, el estado y la lista de reproducción en el marco.

> [!Note]  
> Para mantener la compatibilidad con versiones de Windows Media Player Mobile anteriores a Windows Media Player 10 Mobile, el uso de "Marquis" en un archivo de definición de máscara todavía se considera válido.

 

Para obtener más información sobre la sección marquesina, vea [marquesina](marquee.md) en la referencia de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




