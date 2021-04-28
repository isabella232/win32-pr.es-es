---
description: Información Protección de recursos de Windows claves del Registro
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Información Protección de recursos de Windows claves del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1beeea49f06da182b5ebba38d09227134a6d92c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088783"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Información Protección de recursos de Windows claves del Registro

## <a name="platform"></a>Plataforma

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** baja  


## <a name="description"></a>Descripción

Se han agregado recursos del sistema adicionales Protección de recursos de Windows configuración de WRP (WRP) en Windows 7, lo que los hace configuración de solo lectura. La gran mayoría de los recursos que recibieron protección adicional son claves de servidor COM del sistema, aunque algunas características han agregado protección de recursos de destino. Microsoft cambió estos recursos para proteger el sistema y otras aplicaciones de la separación entre sí y proporcionar una plataforma coherente y estable en la que las aplicaciones se puedan ejecutar de forma confiable. En el pasado, las aplicaciones podían proporcionar archivos personalizados y usar el registro COM sin protección para cambiar el sistema. En el caso de las aplicaciones anteriores, esto puede degradar los tiempos de ejecución del sistema o cambiar la interfaz en la que otras aplicaciones necesitan funcionar correctamente. En el peor de los casos, estas instalaciones podrían provocar un error del sistema o una degradación con el tiempo. Para proporcionar una mejor experiencia y una plataforma de aplicaciones más estable, bloqueamos estos registros para que solo las actualizaciones de Microsoft pudieran cambiar los componentes del sistema.

Dado que la mayoría de los recursos cambiados son claves COM que usa el sistema, este cambio no afectará a la mayoría de las aplicaciones. Aunque esperamos que la mayoría de las aplicaciones tengan una mejor experiencia en Windows 7 como resultado de estos cambios, un pequeño subconjunto de aplicaciones puede verse afectado negativamente. Las capas de compatibilidad de aplicaciones del sistema resolverán automáticamente los problemas de configuración al decir siempre a la aplicación que se ha cambiado correctamente una configuración, incluso si se ha dado error debido a que se trata de un recurso protegido. Esto evita que las configuraciones de la aplicación se rompa, pero puede causar problemas si es necesario cambiar la configuración para que la aplicación funcione correctamente.

## <a name="manifestation"></a>Manifestación

Las aplicaciones pueden haber modificado esta configuración antes de Windows 7. Tras la instalación en Windows 7, es posible que las aplicaciones encuentren que ciertas características ya no funcionan porque la configuración no refleja lo que esperaba la aplicación.

Hay dos escenarios en los que las aplicaciones pueden encontrar problemas relacionados con esta protección adicional:

-   Aplicaciones que pueden haber estado usando la configuración ahora protegida como almacén de datos o como un punto de extensibilidad poco frecuente o no deseado
-   En raras ocasiones, es posible que el mecanismo de detección utilizado para identificar las configuraciones de aplicaciones no reconozca una configuración determinada y, por tanto, no se aplique la capa de mitigación de compatibilidad de aplicaciones.

## <a name="mitigation"></a>Mitigación

El medio principal de mitigación es la capa de compatibilidad de aplicaciones del sistema, que se aplica automáticamente a las configuraciones de la aplicación cuando se detecta. También puede aplicarlo manualmente a cualquier aplicación mediante la pestaña compatibilidad de las propiedades de la aplicación.

Esta capa resuelve el problema interceptando las operaciones del Registro. En el caso de que la aplicación intentara modificar una configuración de solo lectura (WRP), la capa siempre devuelve éxito, aunque la configuración no se haya cambiado realmente. En la mayoría de las aplicaciones, esto no provocará ningún problema. Sin embargo, existe la posibilidad de que la aplicación necesite que esa configuración cambie para funcionar correctamente, que es el primer escenario descrito anteriormente.

## <a name="solution"></a>Solución

Para los dos escenarios identificados anteriormente:

-   Si la aplicación requiere que se pueda escribir la clave para poder funcionar o usar el almacén de datos, no hay otra solución que cambiar la aplicación para que ya no escriba en esa ubicación.
-   Si la capa de compatibilidad no se aplicó a una instalación, el error de instalación debe detectarse y ofrecerse para aplicarse y volver a ejecutarse. Las aplicaciones también se pueden ejecutar en modo de compatibilidad, en cuyo caso siempre se aplica la capa de mitigación.

## <a name="compatibility-tests"></a>Pruebas de compatibilidad

Cómo detectar si a una aplicación se le aplicó la mitigación de WRP:

-   Windows Installer es consciente de WRP; omite de forma automática y silenciosa los intentos de escribir o modificar un recurso protegido. Si la aplicación se instaló con Windows Installer y se ha habilitado el registro, se registrará una advertencia para cada operación de escritura de clave del Registro que se omitió debido a que es un recurso protegido por WRP.
-   La API de WRP incorpora SfCIsKeyProtected, que puede consultar si una clave del Registro está protegida por WRP en el sistema actual. Consulte la entrada WRP en MSDN en los vínculos siguientes para obtener información adicional sobre el uso de esta API.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Protección de recursos de Windows](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
