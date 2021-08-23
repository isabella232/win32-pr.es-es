---
title: Uso del esquema ADSI
description: Un esquema define el universo de objetos almacenados en un directorio.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Uso del esquema ADSI
- ADSI ADSI , con, esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaf49f75d026f52c644d06a6fe36e4555841e3e7bf587ffeb1e0277d1e5ac99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648825"
---
# <a name="using-the-adsi-schema"></a>Uso del esquema ADSI

Un esquema define el universo de objetos almacenados en un directorio. En Active Directory, el esquema especifica qué atributos puede o debe tener un objeto de servicio de directorio. También especifica el intervalo de valores y la sintaxis de los atributos y si admiten uno o varios valores. En resumen, el esquema se organiza por definiciones de clase, definiciones de atributo y sintaxis de atributo. ADSI proporciona tres interfaces para leer datos de atributos, clases y sintaxis de un esquema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax.**](/windows/desktop/api/Iads/nn-iads-iadssyntax)

Active Directory utiliza un conjunto de objetos de esquema para proporcionar una administración de esquemas extensible dinámicamente. Para obtener más información sobre un objeto desconocido, busque sus objetos de esquema asociados. Para crear una nueva definición de clase o ampliar una definición de clase existente, puede crear o ampliar los objetos de esquema adecuados. Los objetos de esquema se organizan en el contenedor de esquemas de un directorio determinado. Para tener acceso a una clase de esquema de objeto, use la propiedad [**IADs.Schema**](iads-property-methods.md) del objeto para obtener la cadena ADsPath y use esa cadena para enlazar a una [**interfaz IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) en la clase de esquema de objeto.

Para determinar las definiciones de atributo, es decir, el intervalo de valores, la sintaxis, y así sucesivamente, inspeccione los objetos de atributo de esquema para cada propiedad admitida por el objeto de servicio de directorio. Para obtener más información sobre cómo acceder a los objetos de atributo de esquema, vea [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI abstrae los datos de sintaxis según sea necesario y le permite usar [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) para identificar la sintaxis necesaria para representar los datos de objeto.

Para obtener más información sobre el esquema Active Directory, vea [Active Directory Schema](/windows/desktop/AD/active-directory-schema). Para obtener ejemplos de código que se usan para leer el contenedor de esquemas, vea [Leer el esquema](reading-the-schema.md).

 

 