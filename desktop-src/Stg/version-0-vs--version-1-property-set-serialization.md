---
title: Serialización del conjunto de propiedades
description: Hay dos versiones del formato de serialización del conjunto de propiedades.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d8dfc1c51a6d33d6eb6f9c22b513a9a5397c87
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436299"
---
# <a name="property-set-serialization"></a>Serialización del conjunto de propiedades

Hay dos versiones del formato de serialización del conjunto de propiedades. La especificación original describe la versión 0 del formato. Consulte [Format Version (Versión](format-version.md) de formato) para obtener más información. La versión 1 amplía la versión original. Todos los conjuntos de propiedades de la versión 0 son válidos como conjuntos de propiedades de la versión 1. El **campo Versión de** formato del encabezado de un conjunto de propiedades serializado indica la versión.

Los siguientes elementos identifican las diferencias entre los formatos de serialización del conjunto de propiedades de la versión 0 y la versión 1.

-   Compatibilidad con nuevos **valores VARTYPE.** Para obtener más información sobre **los valores VARTYPE** y cómo usarlos, vea el tema Tipos y estructuras de datos [IDispatch]( /previous-versions/ms221600(v=vs.100)) y la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

    Los siguientes **valores VARTYPE** no se admiten en los conjuntos de propiedades de la versión 0, pero se admiten en la versión 1:

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    Además, SafeArrays se puede serializar en un conjunto de propiedades. La presencia de safeArray se indica mediante el bit VT_ARRAY combinado, mediante una operación **OR,** con los elementos de matriz en el miembro **vt** de la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Por ejemplo, una SafeArray de enteros de 4 bytes con signo tiene un tipo de VT_ARRAY \| VT_I4.

    Los siguientes tipos de elemento son válidos para SafeArray en un conjunto de propiedades serializado:

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Cuando se VT_VARIANT tipo de datos , indica que safeArray contiene las estructuras [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Los tipos de estos elementos deben ser de la lista anterior, excepto que no pueden contener tipos VT_VARIANT anidados.
    
    Tenga en cuenta que las implementaciones [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) deben poder recuperarse correctamente devolviendo un error cuando se encuentra un nuevo tipo. por ejemplo, tipos VARENUM.

-   Nombres de propiedad que distinguen mayúsculas de minúsculas. Los nombres de propiedad, por ejemplo los especificados en el método [**IPropertyStorage::WritePropertyNames,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) no distinguen mayúsculas de minúsculas en los conjuntos de propiedades de la versión 0. En los conjuntos de propiedades de la versión 1, los nombres de propiedad pueden distinguen mayúsculas de minúsculas en función del valor de la nueva propiedad Behavior.

    La propiedad Behavior es [Property ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) con un tipo de VT_UI4. Si se establece el bit más bajo de este valor, los nombres del conjunto de propiedades distinguen mayúsculas de minúsculas. Establezca la PROPSETFLAG_CASE_SENSITIVE en el parámetro *grfFlags* del método [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para especificar un conjunto de propiedades que distingue mayúsculas de minúsculas.

-   Nombres de propiedad long. Los nombres de propiedad de los conjuntos de propiedades de la versión 0 deben tener menos o igual que 256 caracteres, incluido el terminador de cadena, para los conjuntos de propiedades de la página de códigos Unicode. Si no están en la página de códigos Unicode, deben tener menos de 256 bytes. Por otro lado, los conjuntos de propiedades de la versión 1 pueden tener nombres de propiedad de longitud ilimitada, aunque siguen estando limitados por el límite de tamaño total del conjunto de propiedades de 256 kilobytes (KB).

Se recomienda que las implementaciones de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creen y mantengan conjuntos de propiedades de la versión 0 de forma predeterminada. Si un llamador solicita posteriormente una característica específica del formato de versión 1, solo entonces debe actualizarse la versión del conjunto de propiedades. Por ejemplo, si se escribe una propiedad de tipo VT_ARRAY o si se escribe un nombre de propiedad long, la implementación debe actualizar el formato del conjunto de propiedades a la versión 1. Se produce una excepción a esta guía si se PROPSETFLAG_CASE_SENSITIVE valor de enumeración en la llamada a [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). En este caso, el conjunto de propiedades debe crearse como un conjunto de propiedades de la versión 1.

 

 