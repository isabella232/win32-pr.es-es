---
description: A medida que crece el número de certificados, las listas de revocación de certificados (CRL) y la lista de certificados de confianza (CTL) de la colección de un usuario, la organización de esos certificados se convierte en un problema.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Almacenes de colección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911777"
---
# <a name="collection-stores"></a>Almacenes de colección

A medida que crece el número de [*certificados*](../secgloss/c-gly.md), [*las listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y la [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL) de la colección de un usuario, la organización de esos certificados se convierte en un problema. Una posible solución es crear almacenes de certificados independientes para mantener distintos tipos de certificados. Esta solución crea un nuevo problema porque es posible que una aplicación necesite buscar en varios almacenes distintos para encontrar un certificado específico. En el uso de almacenes lógicos o de colecciones se resuelve este problema.

Un almacén [*lógico*](../secgloss/l-gly.md) y un almacén de certificados de colección son grupos de almacenes físicos que se muestran en una aplicación como un único almacén. Todos los almacenes de miembros de un almacén lógico o de colección se pueden buscar o enumerar con una única llamada de función a [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) o [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).

El uso de almacenes lógicos o de colecciones también proporciona flexibilidad que es difícil de lograr con los registros de papel. Es posible que un certificado de un solo almacén físico tenga que ser miembro de varios grupos lógicos diferentes. Por lo tanto, un almacén físico individual puede ser miembro de más de un almacén lógico o de colección, tal y como se muestra en la siguiente ilustración.

![almacenes de colección](images/mancert.png)

En esta ilustración se presentan los siguientes conceptos básicos del almacén de certificados lógicos:

-   Un almacén de certificados de colección tiene un puntero al primer bloque de puntero para ese almacén de recopilación.
-   Cada bloque de puntero de un almacén de colección tiene un puntero a un almacén relacionado y un puntero al siguiente bloque de puntero de la colección.
-   Cada almacén relacionado de una colección es un almacén de certificados físico simple.
-   Un almacén de certificados simple puede ser un almacén miembro del mismo nivel en muchos almacenes de colecciones diferentes.
-   Los certificados agregados a un almacén de recopilación se agregan físicamente a uno de los almacenes del mismo nivel de la colección.
-   Puede tener acceso a los certificados de un almacén relacionado cualquier almacén de recopilación en el que el almacén relacionado sea miembro.

Los almacenes de colecciones se compilan en una aplicación abriendo un almacén de recopilación mediante [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) y, a continuación, usando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) para agregar un almacén del mismo nivel abierto al almacén de recopilación. Un almacén relacionado se puede eliminar de un almacén de colección mediante una llamada a [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

 

 
