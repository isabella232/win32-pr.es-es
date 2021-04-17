---
description: El evento ReadyStateChange se envía cuando cambia la propiedad ReadyState del control MSWebDVD.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537689"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ReadyStateChange` evento se envía cuando cambia la propiedad **ReadyState** del control MSWebDVD.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

Especifica el nuevo valor de la propiedad [**ReadyState**](readystate-property.md) .



| Value | Descripción               |
|-------|---------------------------|
| 0     | READYSTATE no \_ inicializado |
| 1     | carga de READYSTATE \_       |
| 2     | se \_ cargó READYSTATE        |
| 3     | READYSTATE \_ interactivo   |
| 4     | se \_ completó READYSTATE      |



 

</dd> </dl>

 

 



