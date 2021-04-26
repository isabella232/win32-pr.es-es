---
description: Impide la generación de instrucciones de importación para destinos especificados denominados en un elemento wsdl:import de un archivo WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995882"
---
# <a name="excludeimport-element"></a>excludeImport, elemento

Impide la generación de instrucciones de importación para destinos especificados denominados en \<wsdl:import> un elemento de un archivo WSDL. Esto se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en WSDL.

El valor de este elemento debe establecerse en el espacio de nombres denominado en el \<wsdl:import> elemento que se va a excluir.

## <a name="usage"></a>Uso

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Especifica un archivo WSDL que se procesará para obtener información del contrato.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




