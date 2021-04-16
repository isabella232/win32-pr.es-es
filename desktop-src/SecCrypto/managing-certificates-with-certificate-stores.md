---
description: Usar las funciones de CryptoAPI para administrar almacenes de certificados y certificados, listas de revocación de certificados y listas de certificados de confianza dentro de esas tiendas.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Administración de certificados con almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567288"
---
# <a name="managing-certificates-with-certificate-stores"></a>Administración de certificados con almacenes de certificados

Durante un período de tiempo, los [*certificados*](../secgloss/c-gly.md) se acumularán en el equipo de un usuario. Las herramientas son necesarias para administrar estos certificados. [*CryptoAPI*](../secgloss/c-gly.md) proporciona esas herramientas como funciones para almacenar, recuperar, eliminar, enumerar (enumerar) y comprobar los certificados. CryptoAPI también proporciona los medios para adjuntar certificados a los mensajes.

CryptoAPI ofrece dos categorías principales de funciones para administrar certificados: funciones que administran [*almacenes de certificados*](../secgloss/c-gly.md)y funciones que funcionan con los certificados, [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y listas de certificados de [*confianza*](../secgloss/c-gly.md) (CTL) dentro de esos almacenes.

Las funciones que administran [*almacenes de certificados*](../secgloss/c-gly.md) incluyen funciones para trabajar con [*almacenes*](../secgloss/v-gly.md)lógicos o virtuales, [*almacenes remotos*](../secgloss/r-gly.md), [*almacenes externos*](../secgloss/e-gly.md)y almacenes que se pueden reubicar.

Los certificados, las [*CRL*](../secgloss/c-gly.md)y las [*CTL*](../secgloss/c-gly.md) se pueden mantener y mantener en [*almacenes de certificados*](../secgloss/c-gly.md). Se pueden recuperar de un almacén donde se han guardado para su uso en procesos de autenticación.

El [*almacén de certificados*](../secgloss/c-gly.md) es fundamental para toda la funcionalidad de certificado. Los certificados se administran en el almacén mediante funciones con un prefijo "cert". Un almacén de certificados típico es una lista vinculada de [*certificados*](../secgloss/c-gly.md) , tal como se muestra en la siguiente ilustración.

![almacén de certificados](images/certstore1.png)

En la ilustración anterior se muestra:

-   Cada [*almacén de certificados*](../secgloss/c-gly.md) tiene un puntero al primer bloque de certificado de ese almacén.
-   Un bloque de certificados incluye un puntero a los datos de ese certificado y un puntero "siguiente" al siguiente bloque de certificados del almacén.
-   El puntero "siguiente" en el último bloque de certificado se establece en **null**.
-   El bloque de datos de un certificado contiene el contexto de certificado de solo lectura y las propiedades extendidas del certificado.
-   El bloque de datos de cada certificado contiene un [*recuento de referencias*](../secgloss/r-gly.md) que realiza un seguimiento del número de punteros al certificado que existe.

Normalmente, los certificados de un [*almacén de certificados*](../secgloss/c-gly.md) se mantienen en algún tipo de almacenamiento permanente, como un archivo de disco o el registro del sistema. Los almacenes de certificados también se pueden crear y abrir de forma estricta en la memoria. Un almacén de memoria proporciona un almacenamiento de certificados temporal para trabajar con certificados que no es necesario mantener.

Las ubicaciones de almacén adicionales permiten mantener y buscar almacenes en varias partes del registro de un equipo local o, con los permisos adecuados establecidos, en el registro de un equipo remoto.

Cada usuario tiene un almacén personal en el que se almacenan los certificados del usuario. Mi almacén puede estar en cualquiera de las diversas ubicaciones físicas, incluido el registro en un equipo local o remoto, un archivo de disco, una base de datos, un servicio de directorio, una [*tarjeta inteligente*](../secgloss/s-gly.md)u otra ubicación. Aunque se puede almacenar cualquier certificado en mi almacén, este almacén se debe reservar para los certificados personales de un usuario: los certificados usados para firmar y descifrar los mensajes del usuario.

El uso de certificados para la autenticación depende de la emisión de certificados por parte de un emisor de certificados de confianza. Normalmente, los certificados de los emisores de certificados de confianza se mantienen en el almacén raíz, que actualmente se mantiene en una subclave del registro. En el contexto de CryptoAPI, el almacén raíz está protegido y los cuadros de diálogo de la interfaz de usuario recuerdan al usuario que coloque solo los certificados de confianza en ese almacén. En situaciones de redes empresariales, un administrador del sistema puede insertar (copiar) certificados desde el equipo del controlador de dominio en los almacenes raíz de los equipos cliente. Este proceso proporciona a todos los miembros de un dominio con listas de confianza similares.

Otros certificados se pueden almacenar en el almacén del sistema de la [*entidad de certificación*](../secgloss/c-gly.md) (CA) o en almacenes creados por el usuario y basados en archivos.

Para obtener listas de funciones para usar y mantener almacenes de certificados, consulte [funciones del almacén de certificados](cryptography-functions.md).

Para obtener un ejemplo en el que se usan algunas de estas funciones, vea [programa C de ejemplo: operaciones del almacén de certificados](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar un estado del almacén de certificados](managing-a-certificate-store-state.md)
</dt> <dt>

[Trabajar con certificados en almacenes de certificados](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Vínculos de certificado](certificate-links.md)
</dt> <dt>

[Almacenes de colección](collection-stores.md)
</dt> <dt>

[Almacenes lógicos y físicos](logical-and-physical-stores.md)
</dt> <dt>

[Ubicaciones del almacén del sistema](system-store-locations.md)
</dt> <dt>

[Migración del almacén de certificados](certificate-store-migration.md)
</dt> </dl>

 

 
