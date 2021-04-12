---
title: Evitar el polimorfismo
description: Los nuevos tipos de datos incluyen dos tipos polimórficos, INT \_ ptr y Long \_ PTR.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- polimorfismo 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357628"
---
# <a name="avoiding-polymorphism"></a>Evitar el polimorfismo

Los nuevos tipos de datos incluyen dos tipos polimórficos, **int \_ ptr** y **Long \_ ptr**. En Windows de 32 bits, el **int \_ ptr** se asigna a **int** y **Long \_ ptr** se asigna a **Long**. En Windows de 64 bits, ambos tipos se asignan al tipo intrínseco **\_ \_ Int64** . El compilador MIDL admite estos tipos para llamadas a procedimientos remotos, pero hay una limitación inherente que debe tener en cuenta al usarlos en un entorno distribuido. Asegúrese de comentar el código según corresponda.

Independientemente del tamaño de la plataforma, el tamaño de conexión de estos tipos polimórficos es siempre de 32 bits. Al calcular las referencias de en Windows de 64 bits, el signo de la biblioteca en tiempo de ejecución extiende los valores con signo y asigna cero a los bytes de orden superior para un valor sin signo. Al colocar un valor de 64 bits en la conexión, el tiempo de ejecución trunca los bytes de orden superior. Por lo tanto, solo se pueden usar los valores de 32 bits de orden inferior.

Use los tipos polimórficos solo cuando sea necesario para la migración. En el caso de las nuevas interfaces, use los tipos enteros intrínsecos de MIDL **\_ \_ Int32** e **\_ \_ Int64**, o bien use un tipo de puntero o un identificador de contexto, lo que sea más adecuado para el tipo de datos que se va a transferir.

El compilador de 64 bits admite un nuevo **\_ \_ int3264** intrínseco polimórfico. De nuevo, este tipo se desarrolló para admitir los esfuerzos de migración, en este caso para admitir los tipos de **uint \_ ptr** de forma transparente. (Otro intrínseco, **\_ \_ long3264**, admitirá el tipo de **ULong \_ ptr** ). No use **\_ \_ int3264** directamente; use el tipo **int \_ ptr** cuando necesite un tipo polimórfico por motivos de portabilidad.

 

 




