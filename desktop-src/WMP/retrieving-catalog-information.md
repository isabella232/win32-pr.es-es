---
title: Recuperar información del catálogo
description: Recuperar información del catálogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Reproductor de Windows Media en línea, recuperar información del catálogo
- tiendas en línea, recuperar información del catálogo
- tiendas en línea de tipo 1, recuperación de información del catálogo
- Reproductor de Windows Media en línea, información de diagnóstico sobre catálogos
- tiendas en línea, información de diagnóstico sobre catálogos
- tiendas en línea de tipo 1, información de diagnóstico sobre catálogos
- Reproductor de Windows Media en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- tiendas en línea de tipo 1, catcomp.exe
- catcomp.exe
- información de diagnóstico sobre catálogos
- recuperar información del catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070898"
---
# <a name="retrieving-catalog-information"></a>Recuperar información del catálogo

Puede mostrar información de diagnóstico en un catálogo mediante la ejecución de catcomp con la siguiente sintaxis:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Por ejemplo, el comando siguiente muestra información sobre todo un catálogo, incluida la versión, la configuración regional y la información interna sobre los elementos de catálogo:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



A continuación se muestra información de la pista con el identificador 3256:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




