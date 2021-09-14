---
description: ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo. La asociación incorrecta de un componente a un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074484"
---
# <a name="icem05"></a>ICEM05

ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo. La asociación incorrecta de un componente a un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.

Los ICE del módulo de mezcla se almacenan en un archivo .cub del módulo de mezcla denominado Mergemod.pack y no en el archivo .pack que contiene los ICE usados para la validación del paquete.

## <a name="result"></a>Resultado

ICEM05 publica un error si la base de datos del módulo asocia incorrectamente los componentes y el módulo.

## <a name="example"></a>Ejemplo

ICEM05 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[ModuleSignature Table](modulesignature-table.md)



| ModuleID         | Idioma | Versión |
|------------------|----------|---------|
| Mimodulo. *GUID1* | 3082     | 1.0     |



 

[**Tabla ModuleComponents**](modulecomponents-table.md)



| Componente  | ModuleID            | Idioma |
|------------|---------------------|----------|
| Componente1 | Mimodulo. *GUID1*    | 3082     |
| Componente 2 | OtherModule. *GUID2* | 3082     |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | ComponentID |
|------------|-------------|
| Componente 3 | *GUID4*     |
| Componente 2 | *GUID5*     |



 

El módulo de mezcla ICE notifica el primer error porque la tabla ModuleComponents intenta asociar un componente a otro módulo que no es el módulo actual especificado en la tabla ModuleSignature. Para corregirlo, cambie las columnas ModuleID y Language del registro ModuleComponents para Component2 a la del módulo actual, MyModule. *GUID1*.

El ice del módulo de mezcla notifica el segundo error porque el primer registro de la tabla ModuleComponents intenta asociar Component1 con el módulo. Este componente no existe en la tabla de componentes del módulo merge. Un módulo solo se puede asociar a un componente que existe en el módulo. Para corregirlo, quite el registro del componente inexistente.

El módulo de mezcla ICE notifica el tercer error porque el módulo intenta agregar Component3 a la base de datos de destino. Este componente no se ha asociado al módulo de la tabla ModuleComponents. Para corregir este error, agregue un registro para Component3 a la tabla ModuleComponents.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



