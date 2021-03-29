---
title: Recuperación de información del catálogo
description: Recuperación de información del catálogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player tiendas en línea, recuperar información de catálogo
- tiendas en línea, recuperar información de catálogo
- tipo 1 almacenes en línea, recuperación de información del catálogo
- Windows Media Player tiendas en línea, información de diagnóstico sobre los catálogos
- tiendas en línea, información de diagnóstico en catálogos
- tipo 1 tiendas en línea, información de diagnóstico en catálogos
- Windows Media Player tiendas en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- Escriba 1 tiendas en línea, catcomp.exe
- catcomp.exe
- información de diagnóstico sobre los catálogos
- recuperación de información del catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778264"
---
# <a name="retrieving-catalog-information"></a>Recuperación de información del catálogo

Puede mostrar información de diagnóstico en un catálogo ejecutando catcomp con la siguiente sintaxis:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Por ejemplo, el siguiente comando muestra información sobre un catálogo completo, incluida la versión, la configuración regional y la información interna sobre los elementos del catálogo:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



A continuación se muestra información de la pista con el identificador 3256:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




