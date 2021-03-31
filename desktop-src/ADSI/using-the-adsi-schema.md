---
title: Usar el esquema ADSI
description: Un esquema define el universo de objetos almacenados en un directorio.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Usar el esquema ADSI
- ADSI ADSI, usar, esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904825"
---
# <a name="using-the-adsi-schema"></a>Usar el esquema ADSI

Un esquema define el universo de objetos almacenados en un directorio. En Active Directory, el esquema especifica los atributos que un objeto de servicio de directorio puede o debe tener. También especifica el intervalo de valores y la sintaxis de los atributos, y si admiten uno o varios valores. En Resumen, el esquema se organiza por definiciones de clase, definiciones de atributo y sintaxis de atributo. ADSI proporciona tres interfaces para leer los datos de atributos, clases y sintaxis de un esquema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)y [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory usa un conjunto de objetos de esquema para proporcionar administración de esquemas dinámicamente extensible. Para obtener más información acerca de un objeto desconocido, busque los objetos de esquema asociados. Para crear una nueva definición de clase o extender una definición de clase existente, puede crear o extender los objetos de esquema adecuados. Los objetos de esquema se organizan en el contenedor de esquemas de un directorio determinado. Para obtener acceso a una clase de esquema de objeto, use la propiedad [**IADs. Schema**](iads-property-methods.md) del objeto para obtener la cadena ADsPath y use esa cadena para enlazar a una interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) en la clase de esquema de objetos.

Para determinar las definiciones de atributo, es decir, el intervalo de valores, la sintaxis, etc., inspeccione los objetos de atributo de esquema para cada propiedad admitida por el objeto de servicio de directorio. Para obtener más información sobre cómo obtener acceso a los objetos de atributo de esquema, vea [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI abstrae los datos de sintaxis según sea necesario y permite usar [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) para identificar la sintaxis necesaria para representar los datos de objeto.

Para obtener más información acerca del esquema de Active Directory, vea [esquema de Active Directory](/windows/desktop/AD/active-directory-schema). Para obtener ejemplos de código que se usan para leer el contenedor de esquemas, vea [leer el esquema](reading-the-schema.md).

 

 