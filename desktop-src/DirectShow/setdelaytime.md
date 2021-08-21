---
description: El método SetDelayTime establece el tiempo de retraso de la información sobre herramientas asociada al objeto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ebd119f20977c98aa2664518dc2125b7b5c157b44ff53c3a37740bf40a1677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683745"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetDelayTime` método establece el tiempo de retraso de la información sobre herramientas asociada al objeto **MSWebDVD.**

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Especifica el tipo de retraso como entero.



| Valor | Descripción                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Para restablecer el tiempo de retraso de autopop a su valor predeterminado, establezca *iNewVal* en -1.                                                                                                                                                                       |
| 0     | Establezca el período de tiempo que una ventana de información sobre herramientas permanece visible si el puntero está estacionado dentro del rectángulo delimitador de una herramienta.                                                                                                                         |
| 1     | Establezca el período de tiempo que un puntero debe permanecer estacionado dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana Información sobre herramientas.                                                                                                                    |
| 2     | Establezca el tiempo que tardan las ventanas de información sobre herramientas posteriores en aparecer a medida que el puntero se mueve de una herramienta a otra.                                                                                                                          |
| 3     | Establezca todos los tiempos de retraso en proporciones predeterminadas. El tiempo de autopop es diez veces la hora inicial y la hora de volver a mostrar es una quinta parte de la hora inicial. Si se establece esta marca, use un valor positivo de iNewVal para especificar la hora inicial, en milisegundos. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Especifica el retraso, en milisegundos, como un entero.



| Valor                    | Descripción                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Establece el retraso especificado en *iDelayType* en su valor predeterminado. |
| cualquier otro valor negativo | Establece todos los tipos de retraso en su valor predeterminado.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

 

 



