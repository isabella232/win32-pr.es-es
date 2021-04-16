---
title: Habilitar la seguridad COM mediante DCOMCNFG
description: Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695262"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Habilitar la seguridad COM mediante DCOMCNFG

Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro. Mediante el uso de Dcomcnfg.exe, puede habilitar la seguridad en todo el equipo o en todo el proceso. Puede habilitar la seguridad de un equipo determinado para que cuando un proceso no proporcione su propia configuración de seguridad, ya sea mediante programación o a través de valores del registro, se utilicen los valores establecidos por Dcomcnfg.exe. También puede usar Dcomcnfg.exe para habilitar la seguridad solo para una aplicación determinada.

Al habilitar la seguridad, hay dos tareas principales que debe realizar:

-   Establezca un nivel de autenticación que no sea ninguno.
-   Establezca permisos, incluidos los permisos de acceso y de inicio.

Los pasos que se llevan a cabo para realizar estas tareas dependen de si se habilita la seguridad para todo el equipo o solo para una aplicación determinada. Además, es posible que desee establecer otros valores para el equipo o la aplicación.

> [!Note]  
> Debe ser un administrador para ejecutar Dcomcnfg.exe.

 

En los temas siguientes se proporcionan procedimientos paso a paso para establecer la seguridad con Dcomcnfg.exe:

-   [Establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Configuración de la seguridad de Processwide mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[Desactivar la seguridad](turning-off-security.md)
</dt> </dl>

 

 




