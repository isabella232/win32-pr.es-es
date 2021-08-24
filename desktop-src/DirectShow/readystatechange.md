---
description: El evento ReadyStateChange se envía cuando la propiedad ReadyState del control MSWebDVD ha cambiado.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697125"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El evento se envía cuando ha cambiado la `ReadyStateChange` **propiedad ReadyState** del control MSWebDVD.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*Readystate*
</dt> <dd>

Especifica el nuevo valor de la [**propiedad ReadyState.**](readystate-property.md)



| Valor | Descripción               |
|-------|---------------------------|
| 0     | READYSTATE \_ UNINITIALIZED |
| 1     | CARGA \_ DE READYSTATE       |
| 2     | READYSTATE \_ LOADED        |
| 3     | READYSTATE \_ INTERACTIVE   |
| 4     | READYSTATE \_ COMPLETE      |



 

</dd> </dl>

 

 



