---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protección de recursos de Windows adicionales en las claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697786"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Protección de recursos de Windows adicionales en las claves del registro

## <a name="platform"></a>Plataforma

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : baja  


## <a name="description"></a>Descripción

Los recursos adicionales del sistema han agregado la configuración de Protección de recursos de Windows (WRP) en Windows 7, con lo que se convierte en una configuración de solo lectura. La gran mayoría de los recursos que recibieron protección adicional son claves de servidor COM del sistema, aunque algunas características han agregado protección de recursos de destino. Microsoft ha cambiado estos recursos con el fin de proteger el sistema y otras aplicaciones del modo de interrupción y para proporcionar una plataforma coherente y estable en la que las aplicaciones puedan ejecutarse de forma confiable. En el pasado, las aplicaciones podían proporcionar archivos personalizados y utilizar el registro COM sin protección para cambiar el sistema. En el caso de las aplicaciones anteriores, esto puede degradar los tiempos de ejecución del sistema o cambiar la interfaz en la que otras aplicaciones necesitan funcionar correctamente. En el peor de los casos, estas instalaciones podrían producir un error o una degradación del sistema a lo largo del tiempo. Para proporcionar una mejor experiencia y una plataforma de aplicaciones más estable, bloqueamos estos registros para que solo las actualizaciones de Microsoft pudieran cambiar componentes del sistema.

Dado que la mayoría de los recursos cambiados son claves COM utilizadas por el sistema, este cambio no afectará a la mayoría de las aplicaciones. Aunque esperamos que la mayoría de las aplicaciones tengan una mejor experiencia en Windows 7 como resultado de estos cambios, un pequeño subconjunto de aplicaciones puede verse afectado negativamente. Los niveles de compatibilidad de aplicaciones del sistema resolverán automáticamente los problemas de instalación al indicar siempre a la aplicación que se ha cambiado correctamente la configuración, incluso si se ha producido un error debido a que se trata de un recurso protegido. Esto evita que se interrumpan las configuraciones de la aplicación, pero puede causar problemas si es necesario cambiar la configuración para que la aplicación funcione correctamente.

## <a name="manifestation"></a>Manifestación

Las aplicaciones pueden haber modificado esta configuración antes de Windows 7. Tras instalar en Windows 7, las aplicaciones pueden encontrar ciertas características que ya no funcionan porque la configuración no refleja lo que esperaba la aplicación.

Hay dos escenarios en los que las aplicaciones pueden encontrar problemas relacionados con esta protección agregada:

-   Aplicaciones que pueden haber estado usando la configuración protegida ahora como un almacén de datos o como un punto de extensibilidad poco frecuente o imprevisto
-   En raras ocasiones, es posible que el mecanismo de detección usado para identificar las configuraciones de la aplicación no reconozca una configuración determinada, por lo que es posible que no se aplique la capa de mitigación de compatibilidad de aplicaciones.

## <a name="mitigation"></a>Mitigación

El medio principal de mitigación es el nivel de compatibilidad de aplicaciones del sistema, que se aplica automáticamente a las configuraciones de la aplicación cuando se detecta. También puede aplicarla manualmente a cualquier aplicación mediante la pestaña Compatibilidad en las propiedades de la aplicación.

Este nivel resuelve el problema interceptando las operaciones del registro. En el caso de que la aplicación estuviera intentando modificar una configuración de solo lectura (WRP), la capa siempre devuelve Success, aunque la configuración no se haya modificado realmente. Para la mayoría de las aplicaciones, esto no provocará problemas. Sin embargo, existe la posibilidad de que la aplicación necesite que la configuración haya cambiado para funcionar correctamente, que es el primer escenario descrito anteriormente.

## <a name="solution"></a>Solución

Para los dos escenarios identificados anteriormente:

-   Si la aplicación requiere la escritura de la clave para poder funcionar o usar el almacén de datos, no hay ninguna solución que no sea cambiar la aplicación para que ya no escriba en esa ubicación.
-   Si el nivel de compatibilidad no se aplicó a una instalación, se debe detectar el error de instalación y se le puede aplicar y volver a ejecutar. Las aplicaciones también se pueden ejecutar en modo de compatibilidad, en cuyo caso siempre se aplica la capa de mitigación.

## <a name="compatibility-tests"></a>Pruebas de compatibilidad

Cómo detectar si una aplicación tenía una mitigación de WRP aplicada a ella:

-   Windows Installer es consciente de WRP; omite de forma automática y silenciosa los intentos de escribir o modificar un recurso protegido. Si la aplicación se instaló con Windows Installer y se ha habilitado el registro, se registrará una advertencia para cada operación de escritura de clave del registro que se haya omitido debido a que se trata de un recurso protegido por WRP.
-   La API de WRP incorpora SfCIsKeyProtected, que puede consultar si una clave del registro está protegida por WRP en el sistema actual. Vea la entrada de WRP en MSDN en los vínculos siguientes para obtener información adicional sobre el uso de esta API.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Protección de recursos de Windows](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
