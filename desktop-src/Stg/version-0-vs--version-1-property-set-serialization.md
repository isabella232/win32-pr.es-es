---
title: Serialización de conjunto de propiedades
description: Hay dos versiones del formato de serialización del conjunto de propiedades.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c635728e169cdddb20437323a49a18496b3459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271292"
---
# <a name="property-set-serialization"></a>Serialización de conjunto de propiedades

Hay dos versiones del formato de serialización del conjunto de propiedades. La especificación original describe la versión 0 del formato. Vea [versión de formato](format-version.md) para obtener más información. La versión 1 amplía la versión original. Todos los conjuntos de propiedades de la versión 0 son válidos como conjuntos de propiedades de la versión 1. El campo de **versión de formato** en el encabezado de un conjunto de propiedades serializado indica la versión.

Los elementos siguientes identifican las diferencias entre los formatos de serialización de los conjuntos de propiedades de las versiones 0 y 1.

-   Compatibilidad con los nuevos valores de **VARTYPE** . Para obtener más información sobre los valores de **VARTYPE** y cómo usarlos, vea el tema [tipos de datos y estructuras de IDispatch]( /previous-versions/ms221600(v=vs.100)) y la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

    Los siguientes valores de **VARTYPE** no se admiten en los conjuntos de propiedades de la versión 0, pero se admiten en la versión 1:

    VT \_ I1

    VT \_ Vector \| VT \_ I1

    VT \_ int

    VT \_ uint

    VT \_ decimal

    Además, SafeArray se puede serializar en un conjunto de propiedades. La presencia de un SafeArray se indica mediante el bit de matriz de VT \_ combinado, mediante una operación de **o** , con los elementos de la matriz en el miembro de **VT** de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Por ejemplo, una SafeArray de enteros con signo de 4 bytes tiene un tipo de \_ matriz VT de \| VT \_ I4.

    Los siguientes tipos de elemento son válidos para un SafeArray en un conjunto de propiedades serializadas:



|             |          |             |           |
|-------------|----------|-------------|-----------|
| VT \_ I1      | VT \_ UI1  | I2 de VT \_      | VT \_ UI2   |
| VT \_ I4      | VT \_ UI4  | VT \_ int     | VT \_ uint  |
| VT \_ R4      | VT \_ R8   | VT \_ CY      | fecha de VT \_  |
| VT \_ BSTR    | VT \_ bool | VT \_ decimal | ERROR de VT \_ |
| VT ( \_ variante) |          |             |           |



 

Cuando \_ se especifica el tipo de datos de variante de VT, indica que el propio SafeArray contiene estructuras [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Los tipos de estos elementos deben ser de la lista anterior, salvo que no pueden contener tipos Variant de VT anidados \_ .

Tenga en cuenta que las implementaciones de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) deben poder recuperarse correctamente devolviendo un error cuando se encuentra un nuevo tipo. por ejemplo, VARENUM Types.

-   Nombres de propiedad que distinguen mayúsculas de minúsculas. Los nombres de propiedad, por ejemplo los especificados en el método [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) , no distinguen mayúsculas de minúsculas en los conjuntos de propiedades de la versión 0. En los conjuntos de propiedades de la versión 1, los nombres de propiedad pueden distinguir entre mayúsculas y minúsculas según el valor de la nueva propiedad de comportamiento.

    La propiedad Behavior es el ID. de [propiedad 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) con un tipo de VT \_ UI4. Si se establece el bit más bajo de este valor, los nombres de los conjuntos de propiedades distinguen mayúsculas de minúsculas. Establezca la marca PROPSETFLAG distinguir mayúsculas de \_ minúsculas \_ en el parámetro *GrfFlags* del método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para especificar un conjunto de propiedades que distingue mayúsculas de minúsculas.

-   Nombres de propiedad largos. Los nombres de propiedad de los conjuntos de propiedades de la versión 0 deben ser menores o iguales a 256 caracteres, incluido el terminador de cadena, para los conjuntos de propiedades de la página de códigos Unicode. Si no está en la página de códigos Unicode, debe ser inferior a 256 bytes. Por otro lado, los conjuntos de propiedades de la versión 1 pueden tener nombres de propiedad de longitud ilimitada, aunque siguen estando limitados por el límite de tamaño del conjunto de propiedades general de 256 kilobytes (KB).

Se recomienda que las implementaciones de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creen y mantengan conjuntos de propiedades de la versión 0 de forma predeterminada. Si un llamador solicita posteriormente una característica específica del formato de la versión 1, solo debe actualizarse la versión del conjunto de propiedades. Por ejemplo, si se escribe una propiedad de tipo VT \_ array o se escribe un nombre de propiedad largo, la implementación debe actualizar el formato del conjunto de propiedades a la versión 1. Una excepción a esta directriz se produce si \_ \_ se especifica el valor de enumeración que distingue entre mayúsculas y minúsculas PROPSETFLAG en la llamada a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). En este caso, el conjunto de propiedades debe crearse como un conjunto de propiedades de la versión 1.

 

 