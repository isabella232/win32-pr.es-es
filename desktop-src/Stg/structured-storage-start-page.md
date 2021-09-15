---
title: Datos estructurados Storage
description: Structured Storage proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos conocidos como almacenamientos y flujos.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Structured Storage Strctd Stg
- Structured Storage Strctd Stg , página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270588"
---
# <a name="structured-storage"></a>Datos estructurados Storage

## <a name="purpose"></a>Propósito

Structured Storage proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos conocidos como almacenamientos y flujos.

El propósito de structured Storage es reducir las penalizaciones de rendimiento y la sobrecarga asociadas al almacenamiento de objetos independientes en un solo archivo. Structured Storage proporciona una solución mediante la definición de cómo controlar una sola entidad de archivo como una colección estructurada de dos tipos de almacenamientos y flujos de objetos a través de una implementación estándar denominada Archivos compuestos. Esto permite al usuario interactuar y administrar un archivo compuesto como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.

## <a name="where-applicable"></a>Donde sea aplicable

Los Storage estructurados se pueden usar en sistemas operativos basados en COM de Microsoft.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La documentación de Storage estructurada está pensada para programadores experimentados de C y C++ y desarrolladores de sistemas basados en COM.

Structured Storage admite principalmente los lenguajes de programación C y C++, pero cualquier tecnología basada en COM también admitirá cualquier lenguaje de programación que use punteros de interfaz.

Una comprensión sólida de las tecnologías COM es un requisito previo para el uso de desarrollo de structured Storage.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre qué sistemas operativos deben usar un elemento de API determinado, consulte la sección Requisitos de la documentación del elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general](about-structured-storage.md)<br/>                 | Información general sobre Structured Storage.<br/>                                                                                                                                                                                                                                                 |
| [Uso de structured Storage](using-structured-storage.md)<br/> | Uso de información para structured Storage.<br/>                                                                                                                                                                                                                                                     |
| [Referencia](structured-storage-reference.md)<br/>            | Documentación de structured Storage interfaces, funciones, estructuras y enumeraciones específicas.<br/>                                                                                                                                                                                             |
| [Muestras](samples.md)<br/>                                   | Ejemplos de código escritos en C++. Para obtener más información, vea [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), Storing [Property Sets](storing-property-sets.md)y Using [Structured Storage](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](../com/the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

