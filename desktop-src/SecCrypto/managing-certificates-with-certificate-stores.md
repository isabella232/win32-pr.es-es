---
description: Uso de funciones cryptoAPI para administrar almacenes de certificados y certificados, listas de revocación de certificados y listas de confianza de certificados dentro de esos almacenes.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Administración de certificados con almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270895"
---
# <a name="managing-certificates-with-certificate-stores"></a>Administración de certificados con almacenes de certificados

Durante un período de tiempo, [*los certificados*](../secgloss/c-gly.md) se acumularán en el equipo de un usuario. Se requieren herramientas para administrar estos certificados. [*CryptoAPI*](../secgloss/c-gly.md) proporciona esas herramientas como funciones para almacenar, recuperar, eliminar, enumerar y comprobar certificados. CryptoAPI también proporciona los medios para adjuntar certificados a los mensajes.

CryptoAPI ofrece dos categorías principales de funciones para [](../secgloss/c-gly.md)administrar certificados: funciones que administran almacenes de certificados y funciones que funcionan con los certificados, listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y listas de confianza de certificados [](../secgloss/c-gly.md) (CL) dentro de esos almacenes.

Las funciones que administran [*almacenes de certificados*](../secgloss/c-gly.md) incluyen funciones [](../secgloss/e-gly.md)para trabajar con almacenes lógicos o [*virtuales,*](../secgloss/v-gly.md)almacenes [*remotos,*](../secgloss/r-gly.md)almacenes externos y almacenes que se pueden reubicar.

Los certificados, [*las CRL*](../secgloss/c-gly.md)y [*las CL*](../secgloss/c-gly.md) se pueden conservar y mantener en los [*almacenes de certificados*](../secgloss/c-gly.md). Se pueden recuperar de un almacén donde se han persistente para su uso en procesos de autenticación.

El [*almacén de certificados*](../secgloss/c-gly.md) es fundamental para toda la funcionalidad del certificado. Los certificados se administran en el almacén mediante funciones con un prefijo "Cert". Un almacén de certificados típico es una lista vinculada de [*certificados,*](../secgloss/c-gly.md) como se muestra en la ilustración siguiente.

![almacén de certificados](images/certstore1.png)

En la ilustración anterior se muestra:

-   Cada [*almacén de certificados*](../secgloss/c-gly.md) tiene un puntero al primer bloque de certificados de ese almacén.
-   Un bloque de certificado incluye un puntero a los datos de ese certificado y un puntero "next" al siguiente bloque de certificado del almacén.
-   El puntero "next" del último bloque de certificado se establece en **NULL.**
-   El bloque de datos de un certificado contiene el contexto del certificado de solo lectura y las propiedades extendidas del certificado.
-   El bloque de datos de cada certificado contiene un [*recuento de referencias*](../secgloss/r-gly.md) que realiza un seguimiento del número de punteros al certificado que existen.

Normalmente, los certificados [*de un*](../secgloss/c-gly.md) almacén de certificados se mantienen en algún tipo de almacenamiento permanente, como un archivo de disco o el registro del sistema. Los almacenes de certificados también se pueden crear y abrir estrictamente en memoria. Un almacén de memoria proporciona almacenamiento de certificados temporal para trabajar con certificados que no es necesario conservar.

Las ubicaciones de almacén adicionales permiten que los almacenes se guarden y busquen en varias partes del registro de un equipo local o, con los permisos adecuados establecidos, en el registro de un equipo remoto.

Cada usuario tiene un almacén Mi personal donde se almacenan los certificados de ese usuario. Mi tienda puede estar en cualquiera de las muchas ubicaciones físicas, incluido el registro en un equipo [](../secgloss/s-gly.md)local o remoto, un archivo de disco, una base de datos, un servicio de directorio, una tarjeta inteligente u otra ubicación. Aunque cualquier certificado se puede almacenar en Mi almacén, este almacén debe reservarse para los certificados personales de un usuario: los certificados que se usan para firmar y descifrar los mensajes de ese usuario.

El uso de certificados para la autenticación depende de que algún emisor de certificados de confianza emita los certificados. Los certificados para emisores de certificados de confianza normalmente se mantienen en el almacén raíz, que actualmente se conserva en una subclave del Registro. En el contexto de CryptoAPI, el almacén raíz está protegido y los cuadros de diálogo de la interfaz de usuario le recordarán al usuario que coloque solo certificados de confianza en ese almacén. En situaciones de red empresarial, un administrador del sistema podría insertar (copiar) los certificados del equipo del controlador de dominio en los almacenes raíz de los equipos cliente. Este proceso proporciona a todos los miembros de un dominio listas de confianza similares.

Otros certificados se pueden almacenar en el [*almacén*](../secgloss/c-gly.md) del sistema de la entidad de certificación (CA) o en almacenes basados en archivos creados por el usuario.

Para obtener listas de funciones para usar y mantener almacenes de certificados, vea [Funciones de almacén de certificados](cryptography-functions.md).

Para obtener un ejemplo en el que se usan algunas de estas funciones, vea Programa C de [ejemplo: Operaciones de almacén de certificados](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de un estado de almacén de certificados](managing-a-certificate-store-state.md)
</dt> <dt>

[Trabajar con certificados en almacenes de certificados](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Vínculos de certificado](certificate-links.md)
</dt> <dt>

[Almacenes de colecciones](collection-stores.md)
</dt> <dt>

[Almacenes lógicos y físicos](logical-and-physical-stores.md)
</dt> <dt>

[Ubicaciones del almacén del sistema](system-store-locations.md)
</dt> <dt>

[Migración del almacén de certificados](certificate-store-migration.md)
</dt> </dl>

 

 
