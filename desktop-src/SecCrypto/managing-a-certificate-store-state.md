---
description: Varias funciones proporcionan servicios para administrar un estado de almacén de certificados.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Administración de un estado de almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270903"
---
# <a name="managing-a-certificate-store-state"></a>Administración de un estado de almacén de certificados

Varias funciones proporcionan servicios para administrar un estado [*de almacén de*](../secgloss/c-gly.md) [*certificados.*](../secgloss/s-gly.md)

Para obtener acceso a los certificados, el almacén de certificados en el que se almacenan debe abrirse mediante una llamada a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) o [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

Normalmente, se abre un almacén de certificados en memoria caché. Puede ser un nuevo almacén o su contenido se puede cargar desde el registro local, el registro en un equipo remoto, un archivo de disco, un mensaje PKCS 7 u otro \# origen.

Las funciones de almacén de certificados CryptoAPI también permiten a un almacén mantener los certificados fuera de la memoria caché en, por ejemplo, una base de datos externa de certificados como la proporcionada por la base de datos del servidor de certificados de Microsoft.

Uno de los parámetros de la [**función CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) *lpszStoreProvider,* determina el tipo de almacén abierto y el proveedor usado para abrir ese almacén. Para obtener ejemplos de apertura de almacenes de certificados mediante varios proveedores, vea [Ejemplo de código C para abrir almacenes de certificados](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) cierra un almacén de certificados. Cuando se cierra un almacén de certificados, cada uno de los contextos de certificado de ese almacén tiene su recuento [*de*](../secgloss/r-gly.md) referencias reducido en uno. La memoria se libera para los certificados cuyo recuento de referencias va a cero.

Si se establece CERT CLOSE STORE FORCE FLAG con \_ \_ \_ \_ [**CertCloseStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) se cierra el almacén de certificados y se libera memoria para todos sus contextos de certificado, independientemente de su recuento de referencias. En algunos casos, como en programas multiproceso, esto no puede ser deseable. Si se establece CERT CLOSE STORE CHECK FLAG, el almacén se cierra, pero la función devuelve un valor de advertencia si todavía se asigna memoria para los certificados \_ \_ \_ cuyos recuentos de referencias no se han reducido \_ a cero. Si el recuento de referencias de un certificado es mayor que cero, no se ha liberando un duplicado de ese contexto de certificado. Use [**CertFreeCertificateContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)y [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) para liberar los certificados que quedan abiertos.

> [!Note]
> Un [*contexto de certificado*](../secgloss/c-gly.md) es una estructura de tipo CERT [**\_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que tiene, entre otros miembros, un puntero al [*blob*](../secgloss/c-gly.md) de certificado codificado y un puntero a una estructura [**CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) La **estructura CERT \_ INFO** contiene los datos de certificado más significativos. Para obtener más información sobre las estructuras de contexto de [*certificado,*](../secgloss/c-gly.md)lista de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y lista de certificados de confianza [](../secgloss/c-gly.md) (CTL), vea Codificación y codificación de un contexto de [certificado.](encoding-and-decoding-a-certificate-context.md)
> 
> Cada contexto de certificado también contiene [*un recuento de referencias*](../secgloss/r-gly.md) que indica el número de copias de la dirección del contexto que se han asignado. Cada vez que un contexto de certificado se duplica de cualquier manera, su recuento de referencias se incrementa en uno. Cada vez que se libera un puntero a un contexto de certificado, el recuento de referencias en el contexto del certificado se disminuye en uno. Cuando el recuento de referencias en un contexto de certificado alcanza cero, se desasigna la memoria que mantiene el contexto. La memoria asignada para un contexto de certificado también se desasigna cuando ese contexto está en un almacén y el almacén se cierra mediante CERT \_ CLOSE \_ STORE FORCE \_ \_ FLAG. Si la memoria de un contexto está desasignada y los punteros a ese contexto siguen en uso, esos punteros ya no son válidos.

 

[**CertDuplicateStore aumenta**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) el [*número de referencias*](../secgloss/r-gly.md) en el almacén.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) guarda el contenido de un almacén en un archivo de disco o una ubicación de memoria, y

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) administra un almacén mientras está abierto. Se puede notificar a una aplicación con un almacén abierto cuando el estado persistente de ese almacén ha cambiado en algún otro proceso. Esto puede ocurrir si se copian nuevos certificados en el almacén del equipo local desde un equipo de control de dominio.

Cuando se detectan cambios, el almacén almacenado en caché puede volver a sincronizar su almacén almacenado en caché para que coincida con el estado persistente del almacén. [**CertControlStore también**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) admite un proceso que copia los cambios del almacén almacenado en caché en el almacenamiento permanente cuando estos cambios en el almacén almacenado en caché no se guardan automáticamente.

Los contextos de certificado similares al almacén de certificados pueden tener propiedades extendidas. [**CertSetStoreProperty agrega**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) propiedades extendidas a un almacén de certificados. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) recupera las propiedades establecidas en un almacén de certificados. Actualmente, la única propiedad predefinida del almacén de certificados es el nombre localizado de un almacén.

 

 
