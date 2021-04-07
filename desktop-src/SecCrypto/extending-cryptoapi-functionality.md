---
description: No se puede predecir fácilmente el futuro de las comunicaciones seguras y criptográficas.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Extender la funcionalidad de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002914"
---
# <a name="extending-cryptoapi-functionality"></a>Extender la funcionalidad de CryptoAPI

No se puede predecir fácilmente el futuro de las comunicaciones seguras y [*criptográficas*](../secgloss/c-gly.md) . Pueden surgir nuevos tipos de certificados, varias extensiones de certificado pueden encontrar un uso común y se pueden introducir nuevos tipos de mensajes. Debido a esto, la extensibilidad es parte del diseño de las funciones clave de [*CryptoAPI*](../secgloss/c-gly.md) .

Las secciones siguientes presentan información general sobre el uso de OID para extender las funciones de CryptoAPI.



| Tema                                                                              | Contenido                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre OID](oid-overview.md)                                                   | Conceptos fundamentales de OID.                                                                                                           |
| [Crear la nueva funcionalidad](creating-the-new-functionality.md)               | Crear OID y funciones para extender el uso de las API existentes.                                                                     |
| [Registrar la nueva funcionalidad](registering-the-new-functionality.md)         | Configurar nuevas funciones relacionadas con OID.                                                                                               |
| [Instalación de la nueva funcionalidad](installing-the-new-functionality.md)           | Instalación de funciones OID en la memoria para mejorar el rendimiento.                                                                          |
| [Extensión de la funcionalidad de CertOpenStore](extending-certopenstore-functionality.md) | Extensión de la funcionalidad de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) mediante la función de proveedor de almacén de certificados instalable o registrada. |



 

 

 
