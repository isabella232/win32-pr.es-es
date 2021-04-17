---
title: Interfaces de almacenamiento estructurado
description: Los servicios de almacenamiento estructurado se organizan en tres categorías de interfaces.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfaces de almacenamiento estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0010a0d4dec4908111c8a5bb939f795f0a2b2eb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665844"
---
# <a name="structured-storage-interfaces"></a>Interfaces de almacenamiento estructurado

Los servicios de almacenamiento estructurado se organizan en tres categorías de [interfaces](interfaces.md). Cada conjunto representa un nivel sucesivo de direccionamiento indirecto o abstracción entre un archivo compuesto, los objetos que contiene y el medio físico en el que se almacenan estos componentes individuales.

La primera categoría de interfaces consta de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)y [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). Las dos primeras interfaces definen cómo se almacenan los objetos en un archivo compuesto. Estas interfaces proporcionan métodos para abrir los elementos de almacenamiento, confirmar y revertir los cambios, copiar y mover elementos, y leer y escribir secuencias. Estas interfaces no reconocen los formatos de datos nativos de los objetos individuales y, por lo tanto, no tienen ningún método para guardar los objetos en el almacenamiento persistente. La interfaz **IRootStorage** tiene un único método para asociar un documento compuesto con un nombre del sistema de archivos subyacente. Los clientes deben implementar estas interfaces para sus archivos compuestos.

La segunda categoría de interfaces consta de las interfaces [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) , que los objetos implementan para administrar sus datos persistentes. Estas interfaces proporcionan métodos para leer los formatos de datos de objetos individuales y, por tanto, saber cómo almacenarlos. Los objetos son responsables de implementar estas interfaces, ya que los clientes no conocen los formatos de datos nativos de sus objetos anidados. Sin embargo, estas interfaces no tienen ningún conocimiento de los medios de almacenamiento físico específicos.

Una tercera categoría consta de una única interfaz, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), que proporciona métodos para escribir archivos en medios físicos específicos, como un disco duro o una unidad de cinta. Sin embargo, la mayoría de las aplicaciones no implementarán la interfaz **ILockBytes** porque com ya proporciona implementaciones para las dos situaciones más comunes, que son la implementación basada en archivos y la implementación basada en memoria. El objeto de almacenamiento de archivo compuesto llama a los métodos **ILockBytes** que no se llaman directamente en la implementación.

## <a name="compound-file-implementation-limits"></a>Límites de implementación de archivos compuestos

La implementación COM de la arquitectura de almacenamiento estructurado se denomina *archivos compuestos*. Los objetos de almacenamiento, tal como se implementan en archivos compuestos, incluyen una implementación de las interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

Los punteros a la implementación de archivo compuesto de estas interfaces se adquieren llamando a la función [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear un nuevo objeto de archivo compuesto, o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir un archivo compuesto creado previamente.

Un método alternativo para adquirir un puntero a la implementación de archivo compuesto de estas interfaces es mediante una llamada a la función [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) más antigua y limitada. Las cuatro funciones se tratan como implementaciones de archivos compuestos.

La implementación de archivo compuesto puede configurarse para usar sectores de 512 o 4096 bytes, tal y como se define en la estructura [**STGOPTIONS**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) .

La implementación de archivo compuesto de archivos compuestos está sujeta a las siguientes restricciones de implementación.



| Límite                                           | Archivo compuesto                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Límites de tamaño de archivo:                               | 512:2 gigabytes (GB) 4096: hasta límites del sistema de archivos<br/>                                                                                                                    |
| Tamaño máximo del montón necesario para los elementos abiertos:   | 512:4 megabytes (MB) 4096: hasta límites de memoria virtual<br/>                                                                                                                 |
| Se abre la raíz simultánea (abre el mismo archivo): | Si \_ se especifican STGM Read y STGM \_ share \_ Deny \_ Write, los límites se determinan según los límites del sistema de archivos. De lo contrario, hay un límite de 20 aperturas de raíz simultáneas del mismo archivo. |
| Número de elementos de un archivo:                   | 512: ilimitado, pero el rendimiento puede reducirse si el número de elementos en los miles 4096: ilimitado<br/>                                                                         |



 

Debido al límite de tamaño del montón de 4 MB, el número de elementos abiertos en modo de transacción se limita normalmente a varios miles de elementos.

 

