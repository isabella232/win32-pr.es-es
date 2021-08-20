---
title: Características de rendimiento
description: Una llamada a la implementación del archivo compuesto COM de la interfaz IPropertySetStorage para crear un conjunto de propiedades hace que se cree un flujo o almacenamiento mediante una llamada a IStorage CreateStream o IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac11200b021cae1ea1d60438b57530f0dbc8c02ea3d26b5622ab859a99224aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960835"
---
# <a name="performance-characteristics"></a>Características de rendimiento

Una llamada a la implementación de archivos compuestos COM de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear un conjunto de propiedades hace que se cree un flujo o almacenamiento mediante una llamada a [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Se crea un conjunto de propiedades predeterminado en memoria, pero no se vacía en el disco. Cuando hay una llamada a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), funciona dentro del búfer.

Cuando se abre un conjunto de propiedades, [se usa IStorage::OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) [o IStorage::OpenStorage.](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) Toda la secuencia del conjunto de propiedades se lee en memoria contigua. [**Las operaciones IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) funcionan leyendo el búfer de memoria. Por lo tanto, el primer acceso es costoso en términos de tiempo (debido a las lecturas de disco), pero los accesos posteriores son muy eficaces. Las escrituras pueden ser ligeramente más costosas porque es posible que se requieran operaciones SetSize en la secuencia subyacente para garantizar que el espacio en disco esté disponible si se agregan datos.

No se garantiza si [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) vaciará las actualizaciones. En general, el cliente debe suponer que **IPropertyStorage::WriteMultiple** solo actualiza en el búfer de memoria. Para vaciar los datos, se debe llamar [**a IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (última versión).

Este diseño significa que [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) puede tener éxito, pero los datos no se escriben de forma persistente.

> [!Note]  
> Este tamaño de la secuencia del conjunto de propiedades no puede superar los 256 000 bytes.

 

 

 