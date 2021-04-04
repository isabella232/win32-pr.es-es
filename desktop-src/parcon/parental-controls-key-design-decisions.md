---
description: Decisiones de diseño clave de controles parentales
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisiones de diseño clave de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083366"
---
# <a name="parental-controls-key-design-decisions"></a>Decisiones de diseño clave de controles parentales

Las decisiones de diseño principales en el desarrollo de controles parentales de Windows Vista son:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dependencia esencial de la característica control de cuentas de usuario (UAC) de Windows Vista

Una decisión clave de los controles parentales de Windows Vista es basarse en la nueva característica control de cuentas de usuario (UAC) para implementar las identidades de cuenta de derechos reducidas que se necesitan especialmente para las restricciones sin conexión en los usuarios controlados. Para obtener más información acerca de UAC, vea [la historia de desarrollador de Windows Vista y Windows Server 2008: requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10)). En Resumen, cada cuenta con derechos de administrador tiene privilegios para llevar a cabo el rol primario o tutor para ver los datos de registro y establecer directivas. Los controles parentales solo se pueden establecer en los usuarios de derechos estándar (anteriormente denominados cuentas de usuario con privilegios mínimos o LUAs), ya que solo pueden modificar los registros y los valores de configuración con Access Control listas (ACL) configuradas únicamente para que los administradores escriban. En otras palabras:

-   Una identidad primaria o de protección es igual de forma implícita a una cuenta que tenga derechos de administrador.
-   Los usuarios bajo control parental deben ser usuarios estándar.

## <a name="nearly-all-settings-are-available-by-apis"></a>Casi todas las configuraciones están disponibles en las API

Con la excepción de los elementos como las definiciones del sistema de clasificación, las API expuestas también pueden modificar la configuración disponible para su manipulación por parte de la interfaz de usuario de controles parentales. Es necesario que los programas implementen la elevación de derechos administrativos para modificar la configuración, como se indicó anteriormente para UAC.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>El control parental de Windows Vista es una tecnología solo para consumidores

Los controles parentales de Windows Vista no están diseñados para usarse con cuentas de dominio. Como tecnología de consumidor, el control parental no se implementa en las SKU comerciales de Windows Vista. Si un equipo está unido a un dominio, se suprimirán los vínculos de la interfaz de usuario de seguridad de la familia.

Se proporcionará un mecanismo para exponer la funcionalidad del caso unido al dominio, pero solo se pueden configurar cuentas de usuario que no sean de dominio con controles parentales.

 

 
