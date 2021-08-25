---
description: A medida que crece el número de certificados, las listas de revocación de certificados (CRL) y la lista de confianza de certificados (CL) de la colección de un usuario, la organización de esos certificados se convierte en un problema.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Almacenes de colecciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d783aafe6d0ff22cd990195f6bce5ce433f2f01595bed2cf20c5c41ea3a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876924"
---
# <a name="collection-stores"></a>Almacenes de colecciones

A medida que crece el número de [*certificados,*](../secgloss/c-gly.md)listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y listas de confianza de certificados [](../secgloss/c-gly.md) (CTL) en la colección de un usuario, la organización de esos certificados se convierte en un problema. Una posible solución es crear almacenes de certificados independientes para mantener diferentes tipos de certificados. Esta solución crea un nuevo problema porque es posible que una aplicación tenga que buscar en varios almacenes diferentes para encontrar un certificado específico. El uso de almacenes lógicos o de recopilación resuelve este problema.

Un [*almacén lógico y*](../secgloss/l-gly.md) un almacén de certificados de colección son grupos de almacenes físicos que aparecen en una aplicación como un almacén único. Todos los almacenes de miembros de un almacén lógico o de colección se pueden buscar o enumerar con una sola llamada de función a [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) o [**CertEnumCertificatesInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)

El uso de almacenes lógicos o de colección también proporciona flexibilidad que es difícil de lograr con los registros de papel. Es posible que un certificado de un único almacén físico tenga que ser miembro de varios grupos lógicos diferentes. Por lo tanto, un almacén físico individual puede ser miembro de más de un almacén lógico o de colección, como se muestra en la ilustración siguiente.

![almacenes de colecciones](images/mancert.png)

En esta ilustración se presentan los siguientes conceptos básicos y lógicos del almacén de certificados:

-   Un almacén de certificados de colección tiene un puntero al primer bloque de puntero para ese almacén de recopilación.
-   Cada bloque de puntero de un almacén de recopilación tiene un puntero a un almacén relacionado y un puntero al siguiente bloque de puntero de la colección.
-   Cada almacén relacionado de una colección es un almacén de certificados físico simple.
-   Un almacén de certificados simple puede ser un almacén del mismo nivel de miembro en muchos almacenes de colecciones diferentes.
-   Los certificados agregados a un almacén de recopilación se agregan físicamente a uno de los almacenes del mismo nivel de la colección.
-   Cualquier almacén de recopilación en el que el almacén relacionado sea miembro puede acceder a los certificados de un almacén relacionado.

Los almacenes de recopilación se construyen dentro de una aplicación abriendo un almacén de recopilación mediante [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) y, a continuación, usando [**CertAddStoreToCollection para**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) agregar un almacén del mismo nivel abierto al almacén de recopilación. Un almacén relacionado se puede eliminar de un almacén de recopilación llamando a [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

 

 
