---
description: Una aplicación COM+ es básicamente una construcción declarativa que le permite configurar cualquier número de componentes en común. Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configuración de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d6c8caa8dc4ca949a71d9a6b56fd6eae95d415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358909"
---
# <a name="configuring-com-applications"></a>Configuración de aplicaciones COM+

Una aplicación COM+ es básicamente una construcción declarativa que le permite configurar cualquier número de componentes en común. Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.

La configuración es una parte esencial del proceso de desarrollo para aplicaciones COM+. La forma en que se configura una aplicación determinará cómo COM+ proporcionará servicios para ella y cómo se comporta al ejecutarse.

Puede configurar aplicaciones COM+ mediante la herramienta de administración servicios de componentes o los objetos e interfaces de administración que pueden incluirse en scripts que proporcionan la funcionalidad subyacente de la herramienta de administración. Para obtener más información sobre cómo realizar la administración con scripts, vea [Automatización de la administración de COM+.](automating-com--administration.md)

Puede configurar elementos en los niveles siguientes dentro de las aplicaciones COM+:

-   [Nivel de aplicación Configuración](#application-level-settings)
-   [Nivel de componente (nivel de clase) Configuración](#component-level-class-level-settings)
-   [Configuración de nivel de interfaz](#interface-level-setting)
-   [Configuración de nivel de método](#method-level-setting)
-   [Temas relacionados](#related-topics)

La forma en que se instalan los componentes en una aplicación puede afectar a cómo se pueden configurar. Siempre debe instalar componentes en aplicaciones COM+ (en lugar de importarlos). La instalación de componentes los registrará por completo, junto con interfaces y bibliotecas de tipos, en la base de datos de registro de clases COM+ (RegDB) para que pueda configurarlos.

## <a name="application-level-settings"></a>Application-Level Configuración



| Atributo                                                                                        | Descripción                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Activación](context-activation.md)<br/>                                                  | Especifica el tipo de aplicación: aplicación de servidor o aplicación de biblioteca.<br/>                                                                                                            |
| [Habilitación de comprobaciones de acceso](enabling-access-checks-for-an-application.md)<br/>               | Activa y desactiva la comprobación de seguridad.<br/>                                                                                                                                                      |
| [Nivel de seguridad](setting-a-security-level-for-access-checks.md)<br/>                      | Especifica que las comprobaciones de acceso se realizarán en el nivel de proceso (niveles de comprobación de acceso generados a partir de roles) o tanto en el proceso como en los niveles de componente (seguridad basada en roles completa).<br/> |
| [Nivel de autenticación](setting-an-authentication-level-for-a-server-application.md)<br/>  | Establece el nivel de autenticación utilizado en las llamadas a la aplicación.<br/>                                                                                                                        |
| [Nivel de suplantación](setting-an-impersonation-level.md)<br/>                             | Establece el nivel de suplantación utilizado en las llamadas a otras aplicaciones.<br/>                                                                                                                        |
| [Cola](creating-queuable-components.md)<br/>                                           | Especifica que los componentes de la aplicación usarán servicios de cola.<br/>                                                                                                                         |
| [Habilitación de CRM](configuring-com--crm-components.md)<br/>                                     | Habilita el uso de administradores de recursos de compensación.<br/>                                                                                                                                           |
| [Ejecución de una aplicación como servicio](com--applications-running-as-service-applications.md)<br/> | Configura e implementa una aplicación de servidor COM+ como un servicio NT.<br/>                                                                                                                    |
| [Servicio SOAP COM+](com--soap-service.md)<br/>                                            | Expone una aplicación COM+ como un servicio web XML.<br/>                                                                                                                                        |
| [Agrupación de aplicaciones](com--application-pooling.md)<br/>                                   | Agrega escalabilidad para procesos de un solo subproceso e se integra con el servicio de reciclaje de aplicaciones COM+.<br/>                                                                               |
| [Reciclaje de aplicaciones](com--application-recycling.md)<br/>                               | Aumenta la estabilidad de la aplicación al cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.<br/>                                                                  |
| [Volcado de proceso](what-s-new-in-com--1-5.md)<br/>                                         | Vuelca todo el estado de un proceso sin terminarlo, con fines de depuración.<br/>                                                                                                      |
| Apagado del proceso del servidor<br/>                                                               | Cierra un proceso después de un período de inactividad especificado.<br/>                                                                                                                                      |
| Permisos<br/>                                                                           | Deshabilita los cambios en las opciones de configuración, incluida la eliminación.<br/>                                                                                                                          |
| Identidad de seguridad<br/>                                                                     | Especifica la identidad con la que se ejecuta la aplicación.<br/>                                                                                                                                 |
| Inicio en el depurador<br/>                                                                    | Especifica que la aplicación se va a iniciar en un depurador, con la configuración de línea de comandos especificada por el usuario.<br/>                                                                                |
| Habilitar compatibilidad con 3GB<br/>                                                                    | Habilita el uso del espacio de direcciones de memoria de proceso extendido.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level (nivel de clase) Configuración




| Atributo | Descripción | 
|-----------|-------------|
| <a href="configuring-transactions.md">Transactions</a><br /> | Establece los requisitos de transacción automática Deshabilitado, No admitido, Admitido, Requerido o Requiere nuevo.<br /> | 
| <a href="setting-the-synchronization-attribute.md">Sincronización</a><br /> | Establece los requisitos de sincronización Deshabilitado, No admitido, Admitido, Requerido o Requiere nuevo.<br /> | 
| <a href="enabling-jit-activation-for-a-component.md">Activación JIT</a><br /> | Habilita la activación Just-In-Time.<br /> | 
| <a href="configuring-a-component-to-be-pooled.md">Agrupación de objetos</a><br /> | Habilita la agrupación de objetos. Se pueden configurar los valores mínimo y máximo de tamaño de grupo y tiempo de espera del objeto.<br /> | 
| <a href="specifying-an-object-constructor-string-for-a-component.md">Construcción de objetos</a><br /> | Habilita la construcción de objetos con parámetros con una cadena de constructor especificada administrativamente. <br /><blockquote>[!Note]<br />La cadena de constructor no debe usarse para almacenar información confidencial de seguridad.</blockquote><br /> | 
| <a href="enabling-access-checks-at-the-component-level.md">Comprobaciones de acceso de nivel de componente</a><br /> | Activa o desactiva la comprobación de seguridad basada en roles de nivel de componente.<br /> | 
| <a href="assigning-roles-to-components--interfaces--or-methods.md">Asignación de roles declarativa</a><br /> | Habilita la asignación explícita de roles al componente.<br /> | 
| <a href="persistent-client-side-failures.md">Clase de excepción queueing</a><br /> | Indica una clase de excepción para controlar los errores del lado cliente.<br /> | 
| <a href="com--instrumentation-concepts.md">Eventos y estadísticas de instrumentación</a><br /> | Habilita los informes detallados de eventos del sistema y estadísticas de objetos.<br /> | 
| <a href="context-activation.md">Contexto de activación</a><br /> | Habilita la activación forzada de un objeto en el contexto del autor de la llamada o en el contexto predeterminado.<br /> | 
| <a href="what-s-new-in-com--1-5.md">Creación de componentes privados</a><br /> | Marca el componente como privado para la aplicación. Otros componentes de la misma aplicación solo pueden ver y activar un componente privado.<br /> | 




 

## <a name="interface-level-setting"></a>Interface-Level configuración



| Atributo                                                                                           | Descripción                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [En cola](creating-queuable-components.md)<br/>                                               | Indica una interfaz que se puede colar, definida en IDL.<br/>                                                                       |
| [Asignación de roles declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita la asignación explícita de roles a la interfaz, así como los roles heredados implícitamente del nivel de componente.<br/> |



 

## <a name="method-level-setting"></a>Method-Level configuración



| Atributo                                                                                           | Descripción                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Auto-done](enabling-auto-done-for-a-method.md)<br/>                                         | Desactiva automáticamente el objeto en la devolución del método y vota en la transacción.<br/>                                                       |
| [Asignación de roles declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Permite la asignación explícita de roles al método, así como roles heredados implícitamente de los niveles de interfaz y componente.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la administración de COM+](automating-com--administration.md)
</dt> <dt>

[Creación de aplicaciones COM+](creating-com--applications.md)
</dt> <dt>

[Implementación de aplicaciones COM+](deploying-com--applications.md)
</dt> </dl>

 

 




