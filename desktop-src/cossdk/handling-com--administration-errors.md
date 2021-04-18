---
description: Control de errores de administración de COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Control de errores de administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714841"
---
# <a name="handling-com-administration-errors"></a>Control de errores de administración de COM+

Los errores que se generan al usar los objetos COMAdmin se informan de dos maneras, como se indica a continuación:

-   Usar códigos de error específicos de la biblioteca COMAdmin.
-   Uso de información de error extendida disponible en una colección de [**errorInfo**](errorinfo.md) especial.

## <a name="error-codes"></a>Códigos de error

Los códigos de error de administración se administran como cualquier otro mensaje de error COM. En Microsoft Visual C++, estos códigos se devuelven como valores **HRESULT** . En Microsoft Visual Basic, se producen como excepciones que se pueden detectar. En el caso de los programadores de C++, los códigos de error de administración de COM+ se definen en Winerror. h. Para los programadores de Visual Basic, están disponibles a través del IDE de Visual Basic.

## <a name="errorinfo-collection"></a>Colección ErrorInfo

Cuando se produce un error, señalado por algún tipo de código de error, puede estar disponible información más detallada, dependiendo de la naturaleza del error. Los objetos COMAdmin proporcionan información extendida en las circunstancias en las que es difícil determinar la causa exacta del error sin un informe detallado, como con varias operaciones de lectura y escritura.

Por ejemplo, si usa métodos como [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en un objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , puede leer o escribir datos para cada elemento de la colección. Pueden producirse errores complicados y pueden ser difíciles de diagnosticar en función de un solo código de error numérico. Por lo tanto, la biblioteca COMAdmin crea información de error extendida a través de una colección especial.

Cuando la información de error extendida está disponible, se coloca en la colección [**errorInfo**](errorinfo.md) que está relacionada con la colección original que tuvo el error. Para recuperar el informe de errores, obtenga la colección **errorInfo** relacionada con la colección original y examine los elementos que contiene. Puede recuperar la colección **errorInfo** mediante [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en [**COMAdminCatalogCollection**](comadmincatalogcollection.md), y dejar el segundo parámetro en blanco, donde normalmente especificaría la propiedad clave de un elemento primario.

Cuando se produce un error, debe obtener y rellenar inmediatamente la colección [**errorInfo**](errorinfo.md) para la colección en la que se produjo un error, sin realizar ninguna otra operación en esa colección. De lo contrario, se restablece la colección **errorInfo** y no se detalla ese error.

Los elementos de la colección [**errorInfo**](errorinfo.md) exponen las propiedades de informes de errores especiales MajorRef y MinorRef, que detallan la causa concreta del error. Para obtener más información, consulte **errorInfo**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ en transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecer propiedades y guardar cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



