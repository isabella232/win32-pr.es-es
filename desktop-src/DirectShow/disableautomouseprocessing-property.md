---
description: La propiedad DisableAutoMouseProcessing habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propiedad DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494398"
---
# <a name="disableautomouseprocessing-property"></a>Propiedad DisableAutoMouseProcessing

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DisableAutoMouseProcessing` propiedad habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto **MSWebDVD** .

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se va a deshabilitar el procesamiento predeterminado del mouse.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y su valor predeterminado es false. El objeto **MSWebDVD** controla automáticamente las acciones del mouse para los menús en pantalla de DVD de forma predeterminada. los usuarios pueden resaltar y activar los botones de menú sin necesidad de programación especial por parte de la aplicación. Una aplicación puede desactivar esta funcionalidad predeterminada de control del mouse estableciendo esta propiedad en **true**. Cuando el procesamiento automático del mouse está desactivado, una aplicación debe usar los distintos métodos y propiedades relacionados con el botón para controlar los movimientos del mouse y los clics del mouse en los menús en pantalla. Además, una aplicación puede usar los métodos relacionados con el botón para invalidar el control automático del mouse incluso cuando `DisableAutoMouseProcessing` se establece en **false**.

 

 



