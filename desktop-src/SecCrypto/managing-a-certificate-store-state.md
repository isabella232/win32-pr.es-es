---
description: Varias funciones proporcionan servicios para administrar el estado de un almacén de certificados.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Administrar un estado del almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003454"
---
# <a name="managing-a-certificate-store-state"></a>Administrar un estado del almacén de certificados

Varias funciones proporcionan servicios para administrar el [](../secgloss/c-gly.md) [*Estado*](../secgloss/s-gly.md)de un almacén de certificados.

Para obtener acceso a los certificados, el almacén de certificados en el que se almacenan debe abrirse a través de una llamada a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) o [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

Normalmente, un almacén de certificados se abre en la memoria caché. Puede ser un nuevo almacén o su contenido se puede cargar desde el registro local, el registro de un equipo remoto, un archivo de disco, un \# mensaje PKCS 7 o algún otro origen.

Las funciones del almacén de certificados CryptoAPI también permiten que un almacén mantenga certificados fuera de la memoria caché en, por ejemplo, una base de datos externa de certificados como la proporcionada por la base de datos de Microsoft Certificate Server.

Uno de los parámetros de la función [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , *lpszStoreProvider,* determina el tipo de almacén abierto y el proveedor utilizado para abrir ese almacén. Para obtener ejemplos de cómo abrir almacenes de certificados con varios proveedores, vea [código C de ejemplo para abrir almacenes de certificados](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) cierra un almacén de certificados. Cuando se cierra un almacén de certificados, se reduce el [*recuento de referencias*](../secgloss/r-gly.md) de cada uno de los contextos de certificado de ese almacén. La memoria se libera para los certificados cuyo recuento de referencias llega a cero.

La configuración \_ \_ \_ de la marca de forzar el almacén de cierre \_ del certificado con [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) cierra el almacén de certificados y libera la memoria para todos sus contextos de certificado independientemente de su recuento de referencias. En algunos casos, como en los programas multiproceso, esto no puede ser deseable. Si \_ \_ \_ se establece la marca de comprobación de la tienda de cierre \_ del certificado, el almacén está cerrado, pero la función devuelve un valor de ADVERTENCIA Si todavía se asigna memoria para los certificados cuyos recuentos de referencia no se hayan reducido a cero. Si el recuento de referencias de un certificado es mayor que cero, no se ha liberado un duplicado de ese contexto de certificado. Use [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)y [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) para liberar cualquier certificado que quede abierto.

> [!Note]
> Un [*contexto de certificado*](../secgloss/c-gly.md) es una estructura de tipo de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado que tiene, entre otros miembros, un puntero al [*BLOB de certificado*](../secgloss/c-gly.md) codificado y un puntero a una estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . La estructura de **\_ información** de certificado contiene los datos de certificado más importantes. Para obtener más información acerca de las estructuras de contexto de [*certificado*](../secgloss/c-gly.md), [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL) y lista de certificados de [*confianza*](../secgloss/c-gly.md) (CTL), consulte [codificación y descodificación de un contexto de certificado](encoding-and-decoding-a-certificate-context.md).
> 
> Cada contexto de certificado también contiene un [*recuento de referencias*](../secgloss/r-gly.md) que indica el número de copias de la dirección del contexto que se han asignado. Cada vez que un contexto de certificado se duplica de algún modo, su recuento de referencias se incrementa en uno. Cada vez que se libera un puntero a un contexto de certificado, el recuento de referencias en el contexto del certificado se reduce en uno. Cuando el recuento de referencias en un contexto de certificado llega a cero, se anula la asignación de la memoria que contiene el contexto. También se anula la asignación de la memoria asignada para un contexto de certificado cuando ese contexto está en un almacén y el almacén se cierra con la \_ \_ marca de forzar el almacén de cierre de certificado \_ \_ . Si se anula la asignación de la memoria de un contexto y los punteros a ese contexto todavía están en uso, esos punteros ya no son válidos.

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) aumenta el [*recuento de referencias*](../secgloss/r-gly.md) en el almacén.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) guarda el contenido de un almacén en un archivo de disco o en una ubicación de memoria.

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) administra un almacén mientras está abierto. Se puede notificar a una aplicación con un almacén abierto cuando el estado almacenado de ese almacén ha cambiado por algún otro proceso. Esto puede ocurrir si se copiaron nuevos certificados en el almacén del equipo local desde un equipo de control de dominio.

Cuando se detectan cambios, el almacén almacenado en caché puede volver a sincronizar su almacén almacenado en caché para que coincida con el estado guardado del almacén. [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) también admite un proceso que copia los cambios del almacén almacenado en memoria caché en el almacenamiento permanente cuando estos cambios en el almacén almacenado en memoria caché no se guardan automáticamente.

El almacén de certificados, como los contextos de certificado, puede tener propiedades extendidas. [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) agrega propiedades extendidas a un almacén de certificados. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) recupera todas las propiedades establecidas en un almacén de certificados. Actualmente, la única propiedad predefinida del almacén de certificados es el nombre localizado de un almacén.

 

 
