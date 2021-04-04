---
description: 'Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908665"
---
# <a name="excludeimport-element"></a>elemento excludeImport

Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL. Se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones de WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en el WSDL.

El valor de este elemento debe establecerse en el espacio de nombres denominado en el elemento <WSDL: Import> que se va a excluir.

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



 

 




