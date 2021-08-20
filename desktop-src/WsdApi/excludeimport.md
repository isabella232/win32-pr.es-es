---
description: Impide la generación de instrucciones de importación para destinos especificados denominados en un elemento wsdl:import de un archivo WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11ffc6c6ae6b0005de187afef7e8cbe7d36ca45a13350de1d4b59d40744ae980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920903"
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



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




