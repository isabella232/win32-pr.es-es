---
description: El método SetGPRM establece el registro de parámetros general especificado en el valor especificado.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Método SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061612"
---
# <a name="setgprm-method"></a>Método SetGPRM

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetGPRM` método establece el registro de parámetros general especificado en el valor especificado.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica el registro de parámetros general que se establecerá como un entero. El valor entero debe oscilar entre 0 y 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*
</dt> <dd>

Especifica el nuevo valor para el registro como un entero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los registros de parámetros generales, o GPU, son registros de 16 bits que cada disco puede usar de maneras únicas para el almacenamiento temporal de datos. Una aplicación de reproductor no necesita tener acceso a estos registros para ningún control de reproducción o navegación estándar mediante el **objeto MSWebDVD.** Este método se proporciona para las aplicaciones de reproductor que implementan funcionalidad avanzada. No intente modificar los GPRM directamente a menos que tenga un conocimiento exhaustivo de la especificación de DVD y las formas en que se usan los GPRM en el disco concreto que se va a reproducir. El cambio de estos valores puede dar lugar a un comportamiento impredecible.

 

 



