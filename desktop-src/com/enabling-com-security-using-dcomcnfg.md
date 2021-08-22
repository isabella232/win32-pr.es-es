---
title: Habilitación de la seguridad COM mediante DCOMCNFG
description: Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6161cf7418e7eab705203df51710e789ad2ef7d6843051dd35399fb8388f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678695"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Habilitación de la seguridad COM mediante DCOMCNFG

Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro. Mediante el Dcomcnfg.exe, puede habilitar la seguridad en todo el equipo o en todo el proceso. Puede habilitar la seguridad de un equipo determinado para que cuando un proceso no proporcione su propia configuración de seguridad, ya sea mediante programación o a través de valores del Registro, se usarán los valores establecidos por Dcomcnfg.exe. O bien, puede usar Dcomcnfg.exe para habilitar la seguridad solo para una aplicación determinada.

Al habilitar la seguridad, hay dos tareas principales que realizar:

-   Establezca un nivel de autenticación que no sea Ninguno.
-   Establezca permisos, incluidos los permisos de inicio y acceso.

Los pasos necesarios para realizar estas tareas dependen de si está habilitando la seguridad para todo el equipo o solo para una aplicación determinada. Además, puede establecer otros valores para el equipo o la aplicación.

> [!Note]  
> Debe ser administrador para ejecutar Dcomcnfg.exe.

 

En los temas siguientes se proporcionan procedimientos paso a paso sobre cómo establecer la seguridad con Dcomcnfg.exe:

-   [Configuración System-Wide seguridad mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Establecer la seguridad de todo el proceso mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[Desactivar la seguridad](turning-off-security.md)
</dt> </dl>

 

 




