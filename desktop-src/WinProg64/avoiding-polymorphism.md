---
title: Evitar el polimorfismo
description: Los nuevos tipos de datos incluyen dos tipos polimórficos, INT \_ PTR y LONG \_ PTR.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- polymorphism 64-bit Windows programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068304"
---
# <a name="avoiding-polymorphism"></a>Evitar el polimorfismo

Los nuevos tipos de datos incluyen dos tipos polimórficos, **INT \_ PTR** y **LONG \_ PTR.** En los 32 bits Windows, **int \_ PTR** se asigna a **int** y **LONG \_ PTR** a **long**. En el tipo de Windows 64 bits, ambos tipos se asignan al **\_ \_ tipo int64 int64** int. El compilador MIDL admite estos tipos para llamadas a procedimientos remotos, pero hay una limitación inherente que debe tener en cuenta al usarlos en un entorno distribuido. Asegúrese de comentar el código en consecuencia.

Independientemente del tamaño de la plataforma, el tamaño de la conexión de estos tipos polimórficos siempre es de 32 bits. Al desmarque en un Windows de 64 bits, el signo de biblioteca en tiempo de ejecución extiende los valores firmados y asigna cero a los bytes de orden superior para un valor sin signo. Al colocar un valor de 64 bits en la conexión, el tiempo de ejecución trunca los bytes de orden superior. Por lo tanto, solo se pueden usar los valores de 32 bits de orden bajo.

Use los tipos polimórficos solo cuando sea necesario para la porte. En el caso de las interfaces nuevas, use los tipos enteros int32 e **\_ \_ int64** **\_ \_ int32** int intl intL intl intl int, o bien use un tipo de puntero o un identificador de contexto, lo que sea más adecuado para el tipo de datos que se transfieren.

El compilador de 64 bits admite una nueva **\_ \_ int3264 intrínseca polimórfica.** De nuevo, este tipo se desarrolló para admitir los esfuerzos de porte, en este caso para admitir los tipos **\_ UINT PTR** de forma transparente. (Otro **\_ \_ intrínseco, long3264,** admitirá el **tipo \_ ULONG PTR).** No use **\_ \_ int3264** directamente; use el tipo **INT \_ PTR** cuando necesite un tipo polimórfico por motivos de porte.

 

 




