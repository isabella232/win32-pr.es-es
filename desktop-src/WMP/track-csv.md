---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Reproductor de Windows Media en línea, track.csv
- tiendas en línea, track.csv
- tiendas en línea de tipo 1, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465837"
---
# <a name="trackcsv"></a>track.csv

Este archivo contiene una entrada para cada pista del catálogo. Cada entrada es una fila compuesta de los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si entero se indica en la columna Formato , significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.




| Campo | Obligatorio | Formato | Descripción | 
|-------|----------|--------|-------------|
| Trackid | Sí | Entero no negativo. Ejemplo: 32789<br /> | Identificador único proporcionado por el proveedor de contenido. Debe ser menor que 2^32.Sugerencia de rendimiento: si los identificaciónes asignados a las pistas del mismo álbum se numeran consecutivamente, la compresión del catálogo será más eficaz. Sin embargo, no se requiere la numeración consecutiva de pistas de álbum.<br /> | 
| TrackTitle | Sí | Cadena Unicode. Ejemplo: Blues de Raygun Aldes | Nombre de la pista. | 
| Duration | Sí | Entero no negativo. Ejemplo: 543<br /> | Duración de la pista en segundos. | 
| TrackNumber | Sí | Entero no negativo. Ejemplo: 7<br /> | Número de pista en el álbum de la pista. Los números de pista comienzan en 1 y aumentan entre conjuntos de discos. El número de pista debe ser menor que 256. Un número de seguimiento mayor o igual que 256 provocará un comportamiento inesperado en Reproductor de Windows Media. | 
| TrackPrice | Sí | Cadena Unicode. Ejemplo: 0,99 USD. | Realizar un seguimiento del precio. Se debe incluir el símbolo de moneda. La cadena vacía, 0, y - tienen un significado especial. Una cadena vacía indica que el precio es desconocido. Un cero en este campo significa que la pista es gratuita y un guion (-) indica que no se puede comprar la pista. | 
| CanStream | Sí | booleano. Puede ser 0 o 1. Ejemplo: 0<br /> | Indica si se puede transmitir la pista. | 
| CanDownload | Sí | booleano. Puede ser 0 o 1. Ejemplo: 0<br /> | Indica si se puede descargar la pista. | 
| HasPreviewClip | Sí | booleano. Puede ser 0 o 1. Ejemplo: 0<br /> | Indica si la pista tiene un clip de vista previa. | 
| HasVideoClip | Sí | booleano. Puede ser 0 o 1. Ejemplo: 0<br /> | Indica si la pista tiene un clip de vídeo. | 
| ParentalRating | Sí | Enumeración. Puede ser N, E o C.Ejemplo: N<br /> | Indica la clasificación de asesoramiento parental. Los valores N, E y C son normales, explícitos y limpios. | 
| LinkedAlbumID | Sí | Entero no negativo. Debe ser el identificador de un álbum. Ejemplo: 32423 | Identificador del álbum que contiene esta pista.<blockquote>[!Note]<br />Cada pista debe pertenecer a un álbum. Es decir, para cada pista, el campo LinkedAlbumID debe ser igual a uno de los id. del album.csv disco.</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | Sí | Lista de enteros. La lista contiene los IDs de los intérpretes, separados por punto y coma. Ejemplo: 41322;12321; 82123; | Lista de los IDs correspondientes a los intérpretes colaboradores. | 
| Composer | No | Cadena Unicode. Ejemplo: Fuenía | Compositor de la pista. Si el género de la pista no tiene establecido el campo HasComposer, se omitirá el valor Composer campo. Normalmente solo se usa para pistas clásicas o de jazz. | 
| Popularidad | Sí | Entero no negativo o Float.Example: 1252.6<br /> | Determina la posición de la pista en la lista cuando se ordena por popularidad. Un número menor indica una mayor popularidad. | 
| StarRating | No | Float.Example: 4.21<br /> | La clasificación de estrella se redondeará a la estrella 1/4 más cercana Reproductor de Windows Media antes de mostrarse en la Reproductor de Windows Media usuario. | 




 

 

 





