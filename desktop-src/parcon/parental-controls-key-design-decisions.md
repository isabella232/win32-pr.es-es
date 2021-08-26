---
description: Decisiones clave de diseño de los controles parentales
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisiones clave de diseño de los controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef8f1e1d1b629c9fbb4354fb266376453938a35bde80e7b60f57be8f77da70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939295"
---
# <a name="parental-controls-key-design-decisions"></a>Decisiones clave de diseño de los controles parentales

Las decisiones de diseño principales en el desarrollo Windows los controles parentales de Vista son:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dependencia esencial de la Windows control de cuentas de usuario (UAC) de Vista

Una decisión clave para Windows Vista Parental Controls es basarse en la nueva característica control de cuentas de usuario (UAC) para implementar las identidades de cuenta con derechos reducidos, especialmente necesarias para las restricciones sin conexión de los usuarios controlados. Para obtener más información sobre UAC, vea [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10))[El caso del desarrollador de Windows Vista para el control de cuentas de usuario (UAC) ]. En resumen, todas las cuentas con derechos de administrador tienen privilegios de forma eficaz para realizar el rol primario o guardián de ver los datos de registro y establecer directivas. Los controles parentales solo se pueden establecer en usuarios con derechos estándar (anteriormente denominados cuentas de usuario con privilegios mínimos o LUA), ya que solo no pueden modificar los registros y la configuración con listas de Access Control (ACL) configuradas solo para que los administradores escriban. En otras palabras:

-   Una identidad primaria o de protección equivale implícitamente a una cuenta que tiene derechos de administrador.
-   Los usuarios controlados parentalmente deben ser usuarios estándar.

## <a name="nearly-all-settings-are-available-by-apis"></a>Casi todos los Configuración están disponibles en las API

A excepción de elementos como las definiciones del sistema de clasificaciones, las API expuestas también pueden modificar la configuración disponible para su manipulación por parte de los Interfaz de usuario parentales. Es necesario que los programas implementen la elevación a los derechos administrativos para modificar la configuración, como se indicó anteriormente para UAC.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Vista Parental Controls es una tecnología de solo consumidor

Windows Los controles parentales de Vista no están diseñados para usarse con cuentas de dominio. Como tecnología de consumidor, los controles parentales no se implementan en SKU empresariales de Windows Vista. Si un equipo está unido a un dominio, se suprimirán los vínculos de la interfaz de usuario de Seguridad familiar.

Se proporciona un mecanismo para exponer la funcionalidad del caso unido a un dominio, pero solo se pueden configurar cuentas de usuario que no sean de dominio con controles parentales.

 

 
