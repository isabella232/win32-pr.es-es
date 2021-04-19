---
description: 'Evita la generación de instrucciones Import para los destinos especificados denominados en un elemento wsdl: Import en un archivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380779"
---
# <a name="excludeimport-element"></a>elemento excludeImport

Evita la generación de instrucciones Import para los destinos especificados denominados en un \<wsdl:import> elemento de un archivo WSDL. Se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones de WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en el WSDL.

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
| [**mencionados**](wsdl.md)<br/> | Especifica un archivo WSDL que se va a procesar para la información del contrato.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




