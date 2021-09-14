---
description: La propiedad DisableAutoMouseProcessing habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: DisableAutoMouseProcessing (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061685"
---
# <a name="disableautomouseprocessing-property"></a>DisableAutoMouseProcessing (propiedad)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto `DisableAutoMouseProcessing` **MSWebDVD.**

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se debe deshabilitar el procesamiento predeterminado del mouse.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de false. El **objeto MSWebDVD** controla automáticamente las acciones del mouse para los menús de DVD en pantalla de forma predeterminada; los usuarios pueden resaltar y activar botones de menú sin programación especial por parte de la aplicación. Una aplicación puede desactivar esta funcionalidad predeterminada de control del mouse estableciendo esta propiedad en **true.** Cuando se apaga el procesamiento automático del mouse, una aplicación debe usar los distintos métodos y propiedades relacionados con los botones para controlar los movimientos del mouse y los clics del mouse en los menús en pantalla. Además, una aplicación puede usar los métodos relacionados con los botones para invalidar el control automático del mouse incluso cuando `DisableAutoMouseProcessing` se establece en **false.**

 

 



