---
description: Controles parentales y control de cuentas de usuario
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controles parentales y control de cuentas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716039"
---
# <a name="parental-controls-and-user-account-control"></a>Controles parentales y control de cuentas de usuario

Control de cuentas de usuario (UAC) producirá la presencia de cuentas de usuario estándar y de administrador protegido. Un administrador protegido se ejecutará con los mismos derechos que un usuario estándar en uso normal. Para las operaciones con privilegios:

-   A un usuario estándar se le mostrará el cuadro de diálogo interfaz de usuario de credenciales, que requiere la entrada de un nombre de usuario y una contraseña para un administrador protegido o un administrador integrado.
-   Se mostrará un administrador protegido en el cuadro de diálogo de la interfaz de usuario de consentimiento, que requiere la selección de permitir para continuar.

Es importante tener en cuenta que UAC se implementa por proceso, por lo que un proceso se ejecuta con privilegios elevados o no. Por lo general, no es adecuado desde el punto de vista de la seguridad para ejecutar aplicaciones de gran tamaño como siempre elevado. En el caso de controles parentales, el código que debe modificar la configuración debe aislarse mediante una de las dos opciones de implementación:

1.  Cree un pequeño ejecutable para la administración de la configuración que se marca en su manifiesto como que requiere derechos administrativos. La invocación del archivo ejecutable hará que se muestre la interfaz de usuario del consentimiento o las credenciales antes de permitir que se ejecute el proceso.
2.  Proporcione interfaces COM en un archivo DLL de producto que permita la invocación por documentación de UAC. Esto también hará que se muestre la interfaz de usuario de las credenciales o el consentimiento adecuado.

 

 



