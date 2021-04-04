---
title: Operaciones de Access Control y escritura
description: Se producirá un error en las modificaciones de propiedad si el autor de la llamada no tiene derechos suficientes.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- AD operaciones de Access Control y Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904463"
---
# <a name="access-control-and-write-operations"></a>Operaciones de Access Control y escritura

Se producirá un error en las modificaciones de propiedad si el autor de la llamada no tiene derechos suficientes. En el caso de las operaciones de escritura que realizan modificaciones por lotes en varias propiedades, se produce un error en toda la operación si el llamador no tiene los derechos necesarios en una sola de las propiedades modificadas. Por ejemplo, puede crear varias llamadas [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer varias propiedades en un objeto. Sin embargo, al llamar a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para escribir los datos nuevos de la memoria caché local en el directorio, se producirá un error en **SetInfo** si el autor de la llamada no tiene acceso de escritura a todas las propiedades modificadas. Del mismo modo, el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) no establece ninguna propiedad si el autor de la llamada no tiene acceso a todas las propiedades que se están configurando. Por lo tanto, debe procesar varias operaciones de modificación solo si sabe que todas las modificaciones se realizarán correctamente. Para determinar los atributos de un objeto de directorio que el autor de la llamada tiene la capacidad de modificar, lea el atributo **allowedAttributesEffective** del objeto.

Si el autor de la llamada no tiene derechos suficientes para modificar una propiedad, se pueden devolver los siguientes códigos de retorno:

\_propiedad de \_ ADS \_ no \_ establecida e \_ ADS \_ propiedad \_ no \_ modificada

 

 