---
description: El futuro de la criptografía y las comunicaciones seguras no se puede predecir fácilmente.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Extensión de la funcionalidad cryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171029"
---
# <a name="extending-cryptoapi-functionality"></a>Extensión de la funcionalidad cryptoAPI

El futuro de [*la criptografía*](../secgloss/c-gly.md) y las comunicaciones seguras no se puede predecir fácilmente. Podrían surgir nuevos tipos de certificado, varias extensiones de certificado podrían encontrar un uso común y se podrían introducir nuevos tipos de mensaje. Debido a esto, la extensibilidad forma parte del diseño de funciones [*cryptoAPI*](../secgloss/c-gly.md) clave.

En las secciones siguientes se presentan información general sobre el uso de ID para extender las funciones cryptoAPI.



| Tema                                                                              | Contenido                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre OID](oid-overview.md)                                                   | Conceptos fundamentales de OID.                                                                                                           |
| [Creación de la nueva funcionalidad](creating-the-new-functionality.md)               | Crear ID y funciones para ampliar el uso de las API existentes.                                                                     |
| [Registro de la nueva funcionalidad](registering-the-new-functionality.md)         | Configuración de nuevas funciones relacionadas con OID.                                                                                               |
| [Instalación de la nueva funcionalidad](installing-the-new-functionality.md)           | Instalación de funciones de OID en la memoria para mejorar el rendimiento.                                                                          |
| [Extensión de la funcionalidad CertOpenStore](extending-certopenstore-functionality.md) | Extensión de [**la funcionalidad CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) mediante una función de proveedor de almacén de certificados instalable o registrada. |



 

 

 
