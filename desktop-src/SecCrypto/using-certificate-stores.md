---
description: CAPICOM usa certificados digitales para crear firmas, cifrar claves de cifrado de sesión al crear mensajes envoltorios y descifrar claves de sesión cifradas cuando se recibe un mensaje envoltorio.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Uso de almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f687286d40e64e590079d872a0134742d552b66a9926a1febeb5c42ae2ad7566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971620"
---
# <a name="using-certificate-stores"></a>Uso de almacenes de certificados

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM usa certificados digitales para crear firmas, cifrar claves de cifrado de sesión al crear mensajes envoltorios y descifrar claves de sesión [*cifradas*](../secgloss/d-gly.md) cuando se recibe un mensaje envoltorio. De forma predeterminada, CAPICOM usa certificados en mi almacén que tienen una clave privada asociada para la creación de firmas [*digitales*](../secgloss/d-gly.md) y el descifrado de claves de sesión. En la mayoría de los casos, una aplicación nunca tendría que abrir o tratar directamente con un almacén de certificados.

Sin embargo, las aplicaciones que crean mensajes envolventes usan la [*clave pública*](../secgloss/p-gly.md) de cada destinatario previsto de un mensaje envoltorio. Estas claves se recuperan de los certificados de los destinatarios previstos. Por lo tanto, para crear mensajes envoltorios para un grupo de destinatarios previstos, los certificados de esos destinatarios se recopilarán en un almacén de certificados.

En la tabla siguiente se enumeran los almacenes de certificados estándar que normalmente se conservan en una estación de usuario.



| Tienda        | Descripción                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Contiene certificados personales. Estos certificados normalmente tendrán una clave privada asociada.                                                                                                                                                                                                                                                                             |
| Otras personas | Contiene los certificados de aquellos de los que el usuario normalmente envía mensajes envoltorios a o recibe mensajes firmados de .                                                                                                                                                                                                                                                     |
| Entidad de certificación y raíz  | Contiene los [*certificados de las autoridades*](../secgloss/r-gly.md) de certificación en las que el usuario confía para emitir certificados a otros usuarios. Normalmente, los certificados de estos almacenes se suministran con el sistema operativo o con el administrador de red del usuario. Los certificados del almacén raíz suelen ser autofirmados. |



 

Los almacenes CAPICOM CURRENT USER adicionales se pueden crear, abrir y conservar si se da \_ un nombre de almacén diferente como una \_ cadena. Si no existe un almacén con ese nombre, se crea y se abre un almacén vacío. Si existe un almacén, se abre y todos los certificados que se encuentran actualmente en el almacén están disponibles.

En las secciones siguientes se muestran ejemplos de tareas de almacén de certificados:

-   [Abrir el Active Directory almacenar y recuperar certificados](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Agregar certificados a un almacén de certificados](adding-certificates-to-a-certificate-store.md)
-   [Uso de almacenes en ubicaciones diferentes](using-stores-in-different-locations.md)
-   [Recopilación y comprobación de certificados](collecting-and-verifying-certificates.md)

 

 
