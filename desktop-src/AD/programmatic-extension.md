---
title: Extensión de programación
description: Las extensiones de programación tienen varios méritos; sin embargo, una aplicación es opaca; el administrador debe confiar en la documentación incluida en la aplicación de instalación.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extensión de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773117"
---
# <a name="programmatic-extension"></a>Extensión de programación

La ventaja de un archivo LDIF es que el administrador puede examinar su función. Sin embargo, el esquema también se puede extender mediante programación. Las extensiones de programación tienen varios méritos, pero una aplicación es opaca; el administrador debe confiar en la documentación incluida en la aplicación de instalación. El uso de extensiones de esquema mediante programación puede ser una barrera para la implementación de aplicaciones que las usan. Una extensión de programación es invariable. es un archivo ejecutable de Windows NT. No se puede alterar el binario, a diferencia de un archivo LDIF o. csv, que se puede editar de forma inadvertida o malintencionada.

Las ventajas de un archivo LDIF incluyen:

-   Las aplicaciones pueden detectar y recuperarse de errores y proporcionar comentarios de los usuarios.
-   Las aplicaciones pueden administrar Unicode sin tener que recurrir a la codificación Base64.
-   Las aplicaciones pueden aprovechar Windows Installer API de instalación.
-   Las aplicaciones se pueden firmar para establecer la autenticidad.

 

 




