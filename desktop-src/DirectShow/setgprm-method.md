---
description: El método SetGPRM establece el registro del parámetro general especificado en el valor especificado.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Método SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686320"
---
# <a name="setgprm-method"></a>Método SetGPRM

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetGPRM` método establece el registro del parámetro general especificado en el valor especificado.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica el registro de parámetros general que se va a establecer como un entero. El valor entero debe oscilar entre 0 y 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*Nvalor*
</dt> <dd>

Especifica el nuevo valor del registro como un entero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los registros de parámetros generales, o GPRMs, son registros de 16 bits que cada disco puede utilizar de manera única para el almacenamiento de datos temporal. Una aplicación de reproducción no necesita tener acceso a estos registros para cualquier control de navegación o reproducción estándar mediante el objeto **MSWebDVD** . Este método se proporciona para las aplicaciones de reproductor que implementan la funcionalidad avanzada. No intente modificar el GPRMs directamente a menos que tenga un conocimiento exhaustivo de la especificación del DVD y las maneras en las que se usa el GPRMs en el disco determinado que se va a reproducir. Si se cambian estos valores, se puede producir un comportamiento impredecible.

 

 



