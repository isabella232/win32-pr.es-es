---
title: Características de rendimiento
description: Una llamada a la implementación de archivo compuesto COM de la interfaz IPropertySetStorage para crear un conjunto de propiedades provoca la creación de una secuencia o almacenamiento a través de una llamada a IStorage CreateStream (o IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995405"
---
# <a name="performance-characteristics"></a>Características de rendimiento

Una llamada a la implementación de archivo compuesto COM de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear un conjunto de propiedades provoca la creación de una secuencia o almacenamiento a través de una llamada a [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Un conjunto de propiedades predeterminado se crea en memoria, pero no se vacía en el disco. Cuando hay una llamada a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), funciona dentro del búfer.

Cuando se abre un conjunto de propiedades, se usa [IStorage:: OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [IStorage:: OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) . La secuencia del conjunto de propiedades completo se lee en la memoria contigua. A continuación, las operaciones [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) funcionan mediante la lectura del búfer de memoria. Por lo tanto, el primer acceso es costoso en términos de tiempo (debido a las lecturas del disco), pero los accesos posteriores son muy eficaces. Las escrituras pueden ser ligeramente más costosas porque es posible que sea necesario realizar operaciones en la secuencia subyacente para garantizar que el espacio en disco está disponible si se agregan datos.

No se garantiza que [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Vacíe las actualizaciones. En general, el cliente debe suponer que **IPropertyStorage:: WriteMultiple** solo actualiza el búfer de memoria. Para vaciar los datos, se debe llamar a [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (última versión).

Este diseño significa que [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) puede realizarse correctamente, pero los datos no se escriben realmente de forma persistente.

> [!Note]  
> Este tamaño de la secuencia del conjunto de propiedades no puede superar los 256 k bytes.

 

 

 