---
description: CAPICOM utiliza certificados digitales para crear firmas, cifrar las claves de cifrado de la sesión al crear mensajes con doble cifrado y descifrar las claves de sesión cifrada cuando se recibe un mensaje con doble cifrado.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Uso de almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666724"
---
# <a name="using-certificate-stores"></a>Uso de almacenes de certificados

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM utiliza [*certificados digitales*](../secgloss/d-gly.md) para crear firmas, cifrar las claves de cifrado de la sesión al crear mensajes con doble cifrado y descifrar las claves de sesión cifrada cuando se recibe un mensaje con doble cifrado. De forma predeterminada, CAPICOM usa certificados en el almacén My que tienen una clave privada asociada para la creación de [*firmas digitales*](../secgloss/d-gly.md) y el descifrado de clave de sesión. En la mayoría de los casos, una aplicación nunca tendría que abrir o tratar directamente con un almacén de certificados.

Sin embargo, las aplicaciones que crean mensajes con doble cifrado utilizan la [*clave pública*](../secgloss/p-gly.md) de cada destinatario previsto de un mensaje con doble cifrado. Estas claves se recuperan de los certificados de los destinatarios deseados. Por lo tanto, para crear mensajes con doble cifrado para un grupo de destinatarios deseados, los certificados de esos destinatarios se recopilarían en un almacén de certificados.

En la tabla siguiente se enumeran los almacenes de certificados estándar que normalmente se conservan en una estación de usuario.



| Tienda        | Descripción                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Contiene certificados personales. Normalmente, estos certificados tendrán una clave privada asociada.                                                                                                                                                                                                                                                                             |
| Otras personas | Contiene los certificados de los que el usuario normalmente envía o recibe mensajes con signo.                                                                                                                                                                                                                                                     |
| CA y raíz  | Contiene los [*certificados*](../secgloss/r-gly.md) de entidades de certificación en las que el usuario confía para emitir certificados a otros usuarios. Normalmente, los certificados de estos almacenes se suministran con el sistema operativo o el administrador de red del usuario. Los certificados del almacén raíz suelen ser autofirmados. |



 

\_ \_ Se pueden crear, abrir y conservar almacenes de usuarios actuales de CAPICOM adicionales si se asigna un nombre de almacén diferente como una cadena. Si no existe un almacén con ese nombre, se crea y se abre un almacén vacío. Si existe un almacén, se abre y se pone a disposición todos los certificados del almacén.

En las secciones siguientes se muestran ejemplos de tareas de almacén de certificados:

-   [Abrir el Active Directory almacenar y recuperar certificados](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Agregar certificados a un almacén de certificados](adding-certificates-to-a-certificate-store.md)
-   [Usar almacenes en ubicaciones diferentes](using-stores-in-different-locations.md)
-   [Recopilación y comprobación de certificados](collecting-and-verifying-certificates.md)

 

 
