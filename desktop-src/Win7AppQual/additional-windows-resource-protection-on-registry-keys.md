---
description: Protección adicional Windows recursos en claves del Registro
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protección adicional Windows recursos en claves del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1beeea49f06da182b5ebba38d09227134a6d92c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249429"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Protección adicional Windows recursos en claves del Registro

## <a name="platform"></a>Plataforma

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** baja  


## <a name="description"></a>Descripción

Se han agregado recursos del sistema adicionales Windows configuración de Protección de recursos de recursos (WRP) en Windows 7, lo que los hace una configuración de solo lectura. La gran mayoría de los recursos que recibieron protección agregada son claves de servidor COM del sistema, aunque algunas características han agregado protección de recursos de destino. Microsoft cambió estos recursos para proteger el sistema y otras aplicaciones de la separación entre sí y proporcionar una plataforma coherente y estable en la que las aplicaciones se puedan ejecutar de forma confiable. En el pasado, las aplicaciones podían proporcionar archivos personalizados y usar el registro COM sin protección para cambiar el sistema. En el caso de las aplicaciones anteriores, esto puede degradar los entornos de ejecución del sistema o cambiar la interfaz en la que otras aplicaciones necesitan funcionar correctamente. En el peor de los casos, estas instalaciones podrían provocar un error o una degradación del sistema con el tiempo. Para proporcionar una mejor experiencia y una plataforma de aplicación más estable, hemos bloqueado estos registros para que solo las actualizaciones de Microsoft puedan cambiar los componentes del sistema.

Dado que la mayoría de los recursos modificados son claves COM que usa el sistema, este cambio no afectará a la mayoría de las aplicaciones. Aunque esperamos que la mayoría de las aplicaciones tengan una mejor experiencia en Windows 7 como resultado de estos cambios, un pequeño subconjunto de aplicaciones puede verse afectado negativamente. Las capas de compatibilidad de aplicaciones del sistema resolverán automáticamente los problemas de configuración al decir siempre a la aplicación que ha cambiado correctamente una configuración, incluso si se ha dado un error debido a que es un recurso protegido. Esto impide que las configuraciones de la aplicación se rompa, pero puede causar problemas si es necesario cambiar la configuración para que la aplicación funcione correctamente.

## <a name="manifestation"></a>Manifestación

Las aplicaciones pueden haber modificado esta configuración antes de Windows 7. Tras la instalación en Windows 7, es posible que las aplicaciones encuentren que ciertas características ya no funcionan porque la configuración no refleja lo que esperaba la aplicación.

Hay dos escenarios en los que las aplicaciones pueden encontrar problemas relacionados con esta protección agregada:

-   Aplicaciones que pueden haber estado usando la configuración ahora protegida como almacén de datos o como un punto de extensibilidad poco frecuente o no deseado
-   En raras ocasiones, es posible que el mecanismo de detección utilizado para identificar las configuraciones de aplicaciones no reconozca una configuración determinada y, por tanto, no se aplique el nivel de mitigación de compatibilidad de aplicaciones.

## <a name="mitigation"></a>Mitigación

El medio principal de mitigación es la capa de compatibilidad de aplicaciones del sistema, que se aplica automáticamente a las configuraciones de la aplicación cuando se detecta. También puede aplicarlo manualmente a cualquier aplicación mediante la pestaña compatibilidad de las propiedades de la aplicación.

Esta capa resuelve el problema interceptando las operaciones del Registro. En el caso de que la aplicación intentara modificar una configuración de solo lectura (WRP), la capa siempre devuelve éxito, aunque la configuración no se haya cambiado realmente. En la mayoría de las aplicaciones, esto no provocará ningún problema. Sin embargo, existe la posibilidad de que la aplicación necesite cambiar esa configuración para funcionar correctamente, que es el primer escenario descrito anteriormente.

## <a name="solution"></a>Solución

Para los dos escenarios identificados anteriormente:

-   Si la aplicación requiere que se pueda escribir la clave para poder funcionar o usar el almacén de datos, no hay otra solución que cambiar la aplicación para que ya no escriba en esa ubicación.
-   Si la capa de compatibilidad no se aplicó a una instalación, se debe detectar el error de instalación y ofrecerse para que se aplique y se vuelva a ejecutar. Las aplicaciones también se pueden ejecutar en modo de compatibilidad, en cuyo caso siempre se aplica la capa de mitigación.

## <a name="compatibility-tests"></a>Pruebas de compatibilidad

Cómo detectar si a una aplicación se le aplicó la mitigación de WRP:

-   Windows El instalador es consciente de WRP; omite de forma automática y silenciosa los intentos de escribir o modificar un recurso protegido. Si la aplicación se instaló con el instalador de Windows y se ha habilitado el registro, se registrará una advertencia para cada operación de escritura de clave del Registro que se omitió debido a que se trataba de un recurso protegido por WRP.
-   La API de WRP incorpora SfCIsKeyProtected, que puede consultar si una clave del Registro está protegida por WRP en el sistema actual. Consulte la entrada WRP en MSDN en los vínculos siguientes para obtener información adicional sobre el uso de esta API.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Windows Protección de recursos](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
