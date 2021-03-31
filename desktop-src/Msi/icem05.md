---
description: ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo. La asociación incorrecta de un componente con un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082538"
---
# <a name="icem05"></a>ICEM05

ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo. La asociación incorrecta de un componente con un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.

El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.

## <a name="result"></a>Resultado

ICEM05 publica un error si la base de datos del módulo asocia incorrectamente los componentes y el módulo.

## <a name="example"></a>Ejemplo

ICEM05 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[ModuleSignature (tabla)](modulesignature-table.md)



| ModuleID         | Idioma | Versión |
|------------------|----------|---------|
| MyModule. *GUID1* | 3082     | 1,0     |



 

[**Tabla ModuleComponents**](modulecomponents-table.md)



| Componente  | ModuleID            | Idioma |
|------------|---------------------|----------|
| Component1 | MyModule. *GUID1*    | 3082     |
| Component2 | OtherModule. *GUID2* | 3082     |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

El módulo de combinación ICE informa del primer error porque la tabla ModuleComponents intenta asociar un componente a otro módulo que no es el módulo actual especificado en la tabla ModuleSignature. Para corregir esto, cambie las columnas ModuleID y Language del registro ModuleComponents de Component2 por el correspondiente al módulo actual, MyModule. *GUID1*.

El módulo de combinación ICE informa del segundo error porque el primer registro de la tabla ModuleComponents intenta asociar Component1 con el módulo. Este componente no existe en la tabla de componentes del módulo de combinación. Un módulo solo se puede asociar a un componente que existe en el módulo. Para solucionarlo, quite el registro del componente que no existe.

El módulo de combinación ICE informa del tercer error porque el módulo intenta agregar Component3 a la base de datos de destino. Este componente no se ha asociado al módulo en la tabla ModuleComponents. Para corregir este error, agregue un registro para Component3 a la tabla ModuleComponents.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



