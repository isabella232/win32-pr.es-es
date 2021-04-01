---
description: La propiedad DVDUniqueID recupera un número generado por el sistema que identifica de forma única el disco actual.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propiedad DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906628"
---
# <a name="dvduniqueid-property"></a>Propiedad DVDUniqueID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDUniqueID` propiedad recupera un número generado por el sistema que identifica de forma única el disco actual.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que identifica de forma única el disco actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. El número de identificación (ID.) no es absolutamente único, pero es único para todos los propósitos prácticos. El identificador se aplica a todas las copias replicadas de un disco. En otras palabras, todas las copias de una película específica tienen el mismo identificador. El identificador se basa en tamaños de archivo, fechas y otra información, y no en el valor de BCA.

 

 



