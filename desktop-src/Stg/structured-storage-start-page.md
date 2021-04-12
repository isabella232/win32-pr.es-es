---
title: Almacenamiento estructurado
description: El almacenamiento estructurado proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos que se conocen como almacenamientos y secuencias.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strctd de almacenamiento estructurado STG
- Strctd de almacenamiento estructurado STG, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359164"
---
# <a name="structured-storage"></a>Almacenamiento estructurado

## <a name="purpose"></a>Propósito

El almacenamiento estructurado proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos que se conocen como almacenamientos y secuencias.

El propósito del almacenamiento estructurado es reducir las penalizaciones de rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un único archivo. El almacenamiento estructurado proporciona una solución mediante la definición de cómo controlar una sola entidad de archivo como una colección estructurada de dos tipos de flujos y almacenamiento de objetos a través de una implementación estándar denominada archivos compuestos. Esto permite al usuario interactuar con un archivo compuesto y administrarlo como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.

## <a name="where-applicable"></a>Donde sea aplicable

El almacenamiento estructurado puede usarse en sistemas operativos basados en Microsoft COM.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La documentación de almacenamiento estructurado está pensada para programadores de C y C++ con experiencia y desarrolladores de sistemas basados en COM.

El almacenamiento estructurado es compatible principalmente con lenguajes de programación de C y C++; sin embargo, cualquier tecnología basada en COM también admitirá cualquier lenguaje de programación que use punteros de interfaz.

Una comprensión sólida de las tecnologías COM es un requisito previo para el uso de almacenamiento estructurado.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre los sistemas operativos necesarios para usar un determinado elemento de la API, consulte la sección de requisitos de la documentación del elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general](about-structured-storage.md)<br/>                 | Información general sobre el almacenamiento estructurado.<br/>                                                                                                                                                                                                                                                 |
| [Uso de almacenamiento estructurado](using-structured-storage.md)<br/> | Uso de la información para el almacenamiento estructurado.<br/>                                                                                                                                                                                                                                                     |
| [Referencia](structured-storage-reference.md)<br/>            | Documentación de interfaces, funciones, estructuras y enumeraciones específicas de almacenamiento estructurado.<br/>                                                                                                                                                                                             |
| [Ejemplos](samples.md)<br/>                                   | Ejemplos de código escritos en C++. Para obtener más información, vea [nombres en IStorage](names-in-istorage.md), [encabezado del conjunto de propiedades](property-set-header.md), [sección](section.md), almacenamiento de [conjuntos de propiedades](storing-property-sets.md)y [uso de almacenamiento estructurado](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](../com/the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

