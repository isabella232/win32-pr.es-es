---
description: El método SetDelayTime establece el tiempo de retraso para la información sobre herramientas asociada al objeto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494194"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetDelayTime` método establece el tiempo de retraso para la información sobre herramientas asociada al objeto **MSWebDVD** .

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Especifica el tipo de retraso como un entero.



| Value | Descripción                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Para restablecer el tiempo de retraso de autopop en su valor predeterminado, establezca *iNewVal* en-1.                                                                                                                                                                       |
| 0     | Establece el tiempo durante el que una ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta.                                                                                                                         |
| 1     | Establezca el período de tiempo que un puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.                                                                                                                    |
| 2     | Establezca la cantidad de tiempo que tardará en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se mueva de una herramienta a otra.                                                                                                                          |
| 3     | Establecer todos los tiempos de retraso en las proporciones predeterminadas. La hora de autopop es diez veces la hora inicial y la hora de la representación es una quinta la hora inicial. Si se establece esta marca, use un valor positivo de iNewVal para especificar el tiempo inicial, en milisegundos. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Especifica el retraso, en milisegundos, como un entero.



| Value                    | Descripción                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Establece el retraso especificado en *iDelayType* en su valor predeterminado. |
| cualquier otro valor negativo | Establece todos los tipos de retraso en su valor predeterminado.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

 

 



