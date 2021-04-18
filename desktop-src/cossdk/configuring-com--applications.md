---
description: Una aplicación COM+ es esencialmente una construcción declarativa que le permite configurar cualquier número de componentes en común. Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705274"
---
# <a name="configuring-com-applications"></a>Configurar aplicaciones COM+

Una aplicación COM+ es esencialmente una construcción declarativa que le permite configurar cualquier número de componentes en común. Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.

La configuración es una parte esencial del proceso de desarrollo de aplicaciones COM+. La forma de configurar una aplicación determinará el modo en que COM+ proporcionará los servicios y cómo se comporta cuando se ejecuta.

Puede configurar aplicaciones COM+ mediante la herramienta de administración de servicios de componentes o los objetos e interfaces de administración que admiten scripts que proporcionan la funcionalidad subyacente de la herramienta de administración. Para obtener más información sobre cómo realizar la administración con scripts, vea [automatizar la administración de com+](automating-com--administration.md).

Puede configurar los elementos de los siguientes niveles en las aplicaciones COM+:

-   [Configuración de nivel de aplicación](#application-level-settings)
-   [Configuración de nivel de componente (nivel de clase)](#component-level-class-level-settings)
-   [Configuración de nivel de interfaz](#interface-level-setting)
-   [Configuración de nivel de método](#method-level-setting)
-   [Temas relacionados](#related-topics)

La forma de instalar los componentes en una aplicación puede afectar al modo en que se pueden configurar. Siempre debe instalar los componentes en las aplicaciones COM+ (en lugar de importarlos). Al instalar los componentes, se registrarán por completo, junto con las interfaces y las bibliotecas de tipos, en la base de datos de registro de clases COM+ (RegDB) para que pueda configurarlos.

## <a name="application-level-settings"></a>Configuración de Application-Level



| Atributo                                                                                        | Descripción                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Activación](context-activation.md)<br/>                                                  | Especifica el tipo de aplicación: aplicación de servidor o aplicación de biblioteca.<br/>                                                                                                            |
| [Habilitar comprobaciones de acceso](enabling-access-checks-for-an-application.md)<br/>               | Activa y desactiva la comprobación de seguridad.<br/>                                                                                                                                                      |
| [Nivel de seguridad](setting-a-security-level-for-access-checks.md)<br/>                      | Especifica que las comprobaciones de acceso se realizarán en el nivel de proceso (niveles de comprobación de acceso generados a partir de los roles) o en los niveles de componente (seguridad basada en roles).<br/> |
| [Nivel de autenticación](setting-an-authentication-level-for-a-server-application.md)<br/>  | Establece el nivel de autenticación utilizado en las llamadas a la aplicación.<br/>                                                                                                                        |
| [Nivel de suplantación](setting-an-impersonation-level.md)<br/>                             | Establece el nivel de suplantación utilizado en las llamadas a otras aplicaciones.<br/>                                                                                                                        |
| [MSMQ](creating-queuable-components.md)<br/>                                           | Especifica que los componentes de la aplicación usarán los servicios de cola.<br/>                                                                                                                         |
| [Habilitar CRM](configuring-com--crm-components.md)<br/>                                     | Habilita el uso de administradores de compensación de recursos.<br/>                                                                                                                                           |
| [Ejecutar la aplicación como servicio](com--applications-running-as-service-applications.md)<br/> | Configura e implementa una aplicación de servidor COM+ como un servicio NT.<br/>                                                                                                                    |
| [Servicio SOAP de COM+](com--soap-service.md)<br/>                                            | Expone una aplicación COM+ como un servicio Web XML.<br/>                                                                                                                                        |
| [Agrupación de aplicaciones](com--application-pooling.md)<br/>                                   | Agrega escalabilidad para los procesos de un solo subproceso y se integra con el servicio de reciclaje de aplicaciones COM+.<br/>                                                                               |
| [Reciclaje de aplicaciones](com--application-recycling.md)<br/>                               | Aumenta la estabilidad de la aplicación al cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.<br/>                                                                  |
| [Proceso de volcado](what-s-new-in-com--1-5.md)<br/>                                         | Vuelca todo el estado de un proceso sin terminarlo, con fines de depuración.<br/>                                                                                                      |
| Cierre de proceso de servidor<br/>                                                               | Cierra un proceso después de un período de inactividad especificado.<br/>                                                                                                                                      |
| Permisos<br/>                                                                           | Deshabilita los cambios en los valores de configuración, incluida la eliminación.<br/>                                                                                                                          |
| Identidad de seguridad<br/>                                                                     | Especifica la identidad en la que se ejecuta la aplicación.<br/>                                                                                                                                 |
| Iniciar en el depurador<br/>                                                                    | Especifica que la aplicación se iniciará en un depurador con la configuración de línea de comandos especificada por el usuario.<br/>                                                                                |
| Habilitar compatibilidad con 3GB<br/>                                                                    | Habilita el uso del espacio de direcciones de memoria de proceso extendido.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Configuración de Component-Level (nivel de clase)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transactions</a><br/></td>
<td>Establece los requisitos de transacción automática deshabilitado, no admitido, admitido, requerido o requiere nuevo.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Sincronización</a><br/></td>
<td>Establece los requisitos de sincronización deshabilitados, no admitidos, admitidos, obligatorios o requiere nuevos.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">Activación JIT</a><br/></td>
<td>Habilita la activación Just-in-Time.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Agrupación de objetos</a><br/></td>
<td>Habilita la agrupación de objetos. Se pueden configurar los valores de tiempo de espera mínimo y máximo del grupo y el tiempo de espera del objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Construcción de objetos</a><br/></td>
<td>Habilita la construcción de objetos con parámetros con una cadena de constructor especificada administrativamente. <br/>
<blockquote>
[!Note]<br />
La cadena del constructor no se debe utilizar para almacenar información confidencial de seguridad.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Comprobaciones de acceso de nivel de componente</a><br/></td>
<td>Activa o desactiva la comprobación de seguridad basada en roles de nivel de componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Asignación de roles declarativos</a><br/></td>
<td>Habilita la asignación explícita de roles al componente.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Queue (clase de excepción)</a><br/></td>
<td>Indica una clase de excepción para controlar los errores del lado cliente.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Estadísticas y eventos de instrumentación</a><br/></td>
<td>Habilita los informes detallados de eventos del sistema y estadísticas de objetos.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Contexto de activación</a><br/></td>
<td>Habilita la activación forzada de un objeto en el contexto del autor de la llamada o en el contexto predeterminado.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Crear componentes privados</a><br/></td>
<td>Marca el componente como privado para la aplicación. Un componente privado solo se puede visualizar y activar en otros componentes de la misma aplicación.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Interface-Level configuración



| Atributo                                                                                           | Descripción                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [En cola](creating-queuable-components.md)<br/>                                               | Indica una interfaz queuable, definida en IDL.<br/>                                                                       |
| [Asignación de roles declarativos](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita la asignación explícita de roles a la interfaz, así como a los roles heredados implícitamente desde el nivel de componente.<br/> |



 

## <a name="method-level-setting"></a>Method-Level configuración



| Atributo                                                                                           | Descripción                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Auto-Done](enabling-auto-done-for-a-method.md)<br/>                                         | Desactiva automáticamente el objeto en el método y el resultado de la transacción.<br/>                                                       |
| [Asignación de roles declarativos](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita la asignación explícita de roles al método, así como a los roles heredados implícitamente de los niveles de interfaz y de componente.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatizar la administración de COM+](automating-com--administration.md)
</dt> <dt>

[Crear aplicaciones COM+](creating-com--applications.md)
</dt> <dt>

[Implementación de aplicaciones COM+](deploying-com--applications.md)
</dt> </dl>

 

 




