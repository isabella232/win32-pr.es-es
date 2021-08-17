---
description: Control de errores de administración de COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Control de errores de administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965276fff68edf45ae27423ee4ed707e4bb7f1476b0237dab270538e0fa0f1be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306713"
---
# <a name="handling-com-administration-errors"></a>Control de errores de administración de COM+

Los errores que se generan al usar los objetos COMAdmin se notifican de dos maneras, como se muestra a continuación:

-   Usar códigos de error específicos de la biblioteca COMAdmin.
-   Uso de información de error extendida disponible en una colección [**ErrorInfo**](errorinfo.md) especial.

## <a name="error-codes"></a>Códigos de error

Los códigos de error de administración se controlan como lo haría con cualquier mensaje de error COM. En Microsoft Visual C++, estos códigos se devuelven como **valores HRESULT.** En Microsoft Visual Basic, se inician como excepciones que puede detectar. Para los programadores de C++, los códigos de error de administración de COM+ se definen en Winerror.h. Para Visual Basic programadores, están disponibles a través del IDE Visual Basic.

## <a name="errorinfo-collection"></a>Colección ErrorInfo

Cuando se produce un error, señalado por algún tipo de código de error, puede haber información más detallada disponible, en función de la naturaleza del error. Los objetos COMAdmin proporcionan información extendida en circunstancias en las que la causa exacta del error es difícil de determinar sin un informe detallado, como con varias operaciones de lectura y escritura.

Por ejemplo, cuando se usan métodos como [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en un objeto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) puede leer o escribir datos para cada elemento de la colección. Pueden producirse errores complicados y pueden ser difíciles de diagnosticar en función de un único código de error numérico. Por lo tanto, la biblioteca COMAdmin realiza información de errores extendida a través de una colección especial.

Cuando la información de error extendida está disponible, se coloca en la colección [**ErrorInfo**](errorinfo.md) que está relacionada con la colección original que tenía el error. Para recuperar el informe de errores, obtenga la **colección ErrorInfo** relacionada con la colección original y examine los elementos que contiene. Puede recuperar la colección **ErrorInfo** mediante [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en [**COMAdminCatalogCollection,**](comadmincatalogcollection.md)dejando el segundo parámetro en blanco, donde normalmente se especificaría la propiedad Key de un elemento primario.

Cuando se produce un error, debe obtener y rellenar inmediatamente la colección [**ErrorInfo**](errorinfo.md) de la colección que produjo un error, sin realizar ninguna otra operación en esa colección. De lo contrario, **la colección ErrorInfo** se restablece y no detalla ese error.

Los elementos de la [**colección ErrorInfo**](errorinfo.md) exponen las propiedades especiales de informes de errores MajorRef y MinorRef, que detallan la causa concreta del error. Para obtener más información, vea **ErrorInfo**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ dentro de transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Ejemplo introductorio de uso del catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperación de colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



