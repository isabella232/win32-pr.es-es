---
title: Interfaces Storage estructuradas
description: Los Storage estructurados se organizan en tres categorías de interfaces.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfaces Storage estructuradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345c7b10ae4f73a80b3a263b9a9487c2172382b176404871b363aff336441a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661725"
---
# <a name="structured-storage-interfaces"></a>Interfaces Storage estructuradas

Los Storage estructurados se organizan en tres categorías [de interfaces](interfaces.md). Cada conjunto representa un nivel sucesivo de direccionamiento indirecto o abstracción entre un archivo compuesto, los objetos que contiene y los medios físicos en los que se almacenan estos componentes individuales.

La primera categoría de interfaces consta de [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IRootStorage.**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) Las dos primeras interfaces definen cómo se almacenan los objetos dentro de un archivo compuesto. Estas interfaces proporcionan métodos para abrir elementos de almacenamiento, confirmar y revertir cambios, copiar y mover elementos y leer y escribir secuencias. Estas interfaces no reconocen los formatos de datos nativos de los objetos individuales y, por tanto, no tienen métodos para guardar esos objetos en un almacenamiento persistente. La **interfaz IRootStorage** tiene un único método para asociar un documento compuesto a un nombre de sistema de archivos subyacente. Los clientes deben implementar estas interfaces para sus archivos compuestos.

La segunda categoría de interfaces consta de las interfaces [**IPersist,**](/windows/win32/api/objidl/nn-objidl-ipersist) que los objetos implementan para administrar sus datos persistentes. Estas interfaces proporcionan métodos para leer los formatos de datos de objetos individuales y, por tanto, saber cómo almacenarlos. Los objetos son responsables de implementar estas interfaces porque los clientes no conocen los formatos de datos nativos de sus objetos anidados. Sin embargo, estas interfaces no tienen conocimiento de medios de almacenamiento físico específicos.

Una tercera categoría consta de una sola interfaz, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), que proporciona métodos para escribir archivos en medios físicos específicos, como un disco duro o una unidad de cinta. Sin embargo, la mayoría de las aplicaciones no implementarán la interfaz **ILockBytes** porque COM ya proporciona implementaciones para las dos situaciones más comunes, que son la implementación basada en archivos y la implementación basada en memoria. El objeto de almacenamiento de archivos compuesto llama a **los métodos ILockBytes** que no se llaman directamente en la implementación.

## <a name="compound-file-implementation-limits"></a>Límites de implementación de archivos compuestos

La implementación COM de structured Storage arquitectura se denomina *archivos compuestos*. Storage, como se implementa en archivos compuestos, incluyen una implementación de las interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) [**e IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Los punteros a la implementación de archivos compuestos de estas interfaces se adquieren mediante una llamada a la función [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear un nuevo objeto de archivo compuesto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir un archivo compuesto creado previamente.

Un método alternativo para adquirir un puntero a la implementación de archivo compuesto de estas interfaces consiste en llamar a la función [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) anterior y más limitada. Las cuatro funciones se tratan como implementaciones de archivos compuestos.

La implementación de archivo compuesto se puede configurar para usar sectores de 512 o 4096 bytes, tal como se define en la [**estructura STGOPTIONS.**](/windows/win32/api/coml2api/ns-coml2api-stgoptions)

La implementación de archivos compuestos de archivos compuestos está sujeta a las siguientes restricciones de implementación.



| Límite                                           | Archivo compuesto                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Límites de tamaño de archivo:                               | 512: 2 gigabytes (GB) 4096: hasta límites del sistema de archivos<br/>                                                                                                                    |
| Tamaño máximo del montón necesario para los elementos abiertos:   | 512: 4 megabytes (MB) 4096: hasta límites de memoria virtual<br/>                                                                                                                 |
| Se abre la raíz simultánea (se abre el mismo archivo): | Si se especifican STGM READ y STGM SHARE DENY WRITE, los límites del sistema de archivos dictan \_ \_ los \_ \_ límites. De lo contrario, hay un límite de 20 aperturas raíz simultáneas del mismo archivo. |
| Número de elementos de un archivo:                   | 512: Ilimitado, pero el rendimiento puede disminuir si los elementos se numeran en los miles 4096: Ilimitado<br/>                                                                         |



 

Debido al límite de tamaño del montón de 4 MB, el número de elementos abiertos en modo de transacción normalmente se limita a varios miles de elementos.

 

