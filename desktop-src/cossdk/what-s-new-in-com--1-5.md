---
description: LA versión 1.5 de COM+ agrega nuevas características diseñadas para aumentar la escalabilidad, disponibilidad y capacidad de administración generales de las aplicaciones COM+ tanto para desarrolladores como para administradores del sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novedades de COM+ 1.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304886"
---
# <a name="whats-new-in-com-15"></a>Novedades de COM+ 1.5

LA versión 1.5 de COM+ agrega nuevas características diseñadas para aumentar la escalabilidad, disponibilidad y capacidad de administración generales de las aplicaciones COM+ tanto para desarrolladores como para administradores del sistema.

COM+ 1.5 está disponible a partir de Windows XP y Windows Server 2003. Las nuevas características de COM+ 1.5 no están disponibles en Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level de acceso habilitado de forma predeterminada

Como parte de la seguridad mejorada del sistema, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. En versiones anteriores, las comprobaciones de acceso se deshabilitaban de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente. A partir Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Consulte Creación de una nueva aplicación [COM+](creating-a-new-com--application.md) [,](enabling-access-checks-for-an-application.md)Habilitación de comprobaciones de acceso para una aplicación y Habilitación de comprobaciones de acceso en el nivel de componente para obtener más información y procedimientos sobre cómo cambiar la configuración predeterminada. [](enabling-access-checks-at-the-component-level.md)

## <a name="application-pooling"></a>Agrupación de aplicaciones

Con la nueva propiedad ConcurrentApps del objeto [](applications.md) [**COMAdminCatalogObject**](comadmincatalogobject.md) en la colección Applications, la agrupación de aplicaciones COM+ agrega escalabilidad para procesos de un solo subproceso e se integra con el nuevo servicio de reciclaje de aplicaciones COM+. Consulte [Agrupación de aplicaciones COM+](com--application-pooling.md) para obtener información detallada.

## <a name="application-recycling"></a>Reciclaje de aplicaciones

El reciclaje de aplicaciones aumenta significativamente la estabilidad general de las aplicaciones. Dado que el rendimiento de la mayoría de las aplicaciones puede degradarse con el tiempo debido a factores como pérdidas de memoria, dependencia del código de terceros y uso de recursos nocalables, el reciclaje de aplicaciones COM+ proporciona una solución sencilla para apagar correctamente un proceso asociado a una aplicación y reiniciarlo. Consulte [Reciclaje de aplicaciones COM+](com--application-recycling.md) para obtener información detallada. Consulte también "Configuración del reciclaje de procesos" en la Ayuda de administración de servicios de componentes para obtener un procedimiento paso a paso para configurar el reciclaje de procesos.

## <a name="com-partitions"></a>Particiones COM+

En esta versión, COM+ presenta compatibilidad con particiones COM+, una característica que permite instalar y configurar varias versiones de aplicaciones COM+ en la misma máquina. Esta característica puede ahorrarle el costo y el esfuerzo lento de usar varios servidores para administrar versiones diferentes de una aplicación. En una sola máquina, cada partición actúa, en efecto, como un servidor virtual. Después de instalar la aplicación en cada partición, cree conjuntos de particiones que asignen usuarios a los servidores lógicos. Consulte [Particiones COM+](com--partitions.md) para obtener información detallada sobre cómo configurar y administrar particiones COM+. Consulte también "Administración de particiones de aplicación" en la Ayuda de administración de servicios de componentes para procedimientos paso a paso.

## <a name="com-services-without-components"></a>Servicios COM+ sin componentes

Con COM+ 1.5, puede usar los servicios proporcionados por COM+ sin necesidad de compilar un componente para contener los métodos que llaman a esos servicios. Esto beneficia en gran medida a los desarrolladores que no suelen usar componentes, pero que desean usar servicios COM+, como transacciones o el rastreador COM+. Mediante el uso de servicios COM+ sin componentes, los desarrolladores pueden evitar la sobrecarga de crear un componente que se usa para acceder solo a los servicios COM+ que necesitan. Consulte [SERVICIOS COM+ sin componentes para](com--services-without-components.md) obtener información detallada.

## <a name="com-soap-service"></a>Servicio SOAP de COM+

Con COM+ 1.5, ahora puede exponer una aplicación COM+ como un servicio web XML. También puede usar de forma transparente un servicio web XML, ya sea implementado con COM+ o no, como componente COM. Esto significa que puede crear fácilmente nuevos servicios web XML a través de aplicaciones COM+ existentes e incorporar fácilmente servicios web XML en nuevas aplicaciones COM+. Consulte [Servicio SOAP COM+](com--soap-service.md) para obtener información detallada.

## <a name="configurable-isolation-levels"></a>Niveles de aislamiento configurables

Los desarrolladores de COM+ pueden usar la nueva propiedad TxIsolationLevel o la herramienta administrativa Servicios de componentes para configurar el nivel de aislamiento de una aplicación según sea necesario, lo que ayuda a aumentar la simultaneidad, el rendimiento y la escalabilidad. Esta flexibilidad permite que aquellos con la cantidad adecuada de experiencia obtengan cada última onza de rendimiento de sus aplicaciones. Consulte [Configuring Transaction Isolation Levels (Configuración de niveles de aislamiento de transacción)](configuring-transaction-isolation-levels.md) para obtener información detallada.

## <a name="creating-private-components"></a>Creación de componentes privados

En escenarios en los que tiene varios componentes auxiliares en una aplicación que están diseñados para llamarse solo desde otros componentes dentro de esa aplicación, esta versión de COM+ permite usar una nueva propiedad, IsPrivateComponent, para marcar estos componentes como privados. (En la versión anterior de COM+, todos los componentes tenían que ser públicos para tener acceso a los servicios COM+, lo que significa que estos componentes se podían activar desde otras aplicaciones). Solo otros componentes de la misma aplicación pueden ver y activar un componente privado, lo que le proporciona más control sobre qué funcionalidad exponer. Solo necesita documentar y mantener los componentes públicos, al tiempo que usa componentes privados a los que no se puede acceder desde fuera de la aplicación, pero que todavía pueden aprovechar todos los servicios COM+.

## <a name="dtc-security-settings"></a>Seguridad de DTC Configuración

Se han agregado varias nuevas opciones de seguridad para el Microsoft DTC (Coordinador de transacciones distribuidas) (DTC), lo que le permite personalizar los niveles de seguridad para administrar las transacciones distribuidas. Consulte Consideraciones de seguridad de DTC sobre esta configuración y cómo implementarlas.

Para facilitar la autenticación mutua, el DTC está restringido a ejecutarse en la cuenta NetworkService. Consulte Administración de cuentas y privilegios para obtener información detallada.

Para la recuperación con bases de datos XA, se recomienda proporcionar a la cuenta NetworkService los permisos y roles necesarios para realizar esta recuperación. El método exacto para hacerlo es específico de cada base de datos. Vea Deshabilitar transacciones distribuidas nativas y Deshabilitar transacciones TIP y XA para obtener más información.

Para ayudar a proporcionar un sistema más seguro al usar transacciones XA, las plataformas Windows Server 2003 incluyen una nueva entrada del Registro para especificar archivos DLL XA. Al actualizar a Windows Server 2003, puede trabajar con transacciones XA como antes mediante la creación de una entrada del Registro en **\_ HKEY LOCAL \_ MACHINE SOFTWARE \\ Microsoft \\ \\ MSDTC \\ XADLL,** donde el nombre del valor es el nombre del archivo DLL (con el formato *dllname*.dll) y el valor es la ruta de acceso completa del archivo DLL. Debe crear una entrada para cada archivo DLL XA en uso. Si el equipo que ejecuta DTC forma parte de un clúster, la entrada del Registro debe realizarse para cada nodo del clúster. Consulte Administración de transacciones XA para obtener más información.

## <a name="low-memory-activation-gates"></a>Low-Memory puertas de activación

Con esta versión, COM+ comprueba automáticamente la memoria antes de crear un servidor u objeto COM+. Si el porcentaje de memoria virtual disponible para la aplicación está por debajo de un umbral fijo, se produce un error en la activación antes de crear el objeto. Al dar error a estas activaciones que normalmente se ejecutarían, el servicio [COM+ Low-Memory Activation Gates](com--low-memory-activation-gates.md) mejora en gran medida la confiabilidad del sistema.

## <a name="moving-and-copying-com-components"></a>Mover y copiar componentes COM

Con esta versión, COM+ permite mover y copiar los componentes. Esto significa que puede configurar una implementación física única de un componente muchas veces diferentes. Se obtiene la reutilización de componentes en un nivel binario en lugar de en el nivel de código fuente, lo que da como resultado menos código, menores costos de desarrollo y un tiempo de comercialización más rápido. Consulte [Mover componentes](moving-components.md) y copiar componentes [para](copying-components.md) obtener información detallada.

## <a name="network-access"></a>Acceso de red

El acceso a la red COM+ está deshabilitado de forma predeterminada en Windows Server 2003, lo que significa que COM+ solo se puede usar localmente de forma predeterminada. Use el procedimiento siguiente para habilitar el acceso com+ de red.

**Para habilitar el acceso COM+ de red**

1.  En el **menú** Inicio, seleccione **Panel de control** y, a continuación, seleccione Agregar o quitar **programas.**

2.  Haga **clic en Agregar o quitar Windows componentes**.

3.  Seleccione **Servidor de aplicaciones** y haga clic en **Detalles**.

4.  Active la casilla situada junto a **Habilitar el acceso COM+ de red** y, a continuación, haga clic en **Aceptar.**

5.  Haga **clic en** Siguiente para completar el asistente Windows componentes.

6.  Haga **clic en** Finalizar para cerrar el asistente.

El acceso a transacciones de red DTC está deshabilitado de forma predeterminada Windows Server 2003. En estas plataformas, el DTC solo puede realizar transacciones locales de forma predeterminada. Use el procedimiento siguiente para habilitar el acceso DTC de red.

> [!NOTE]
> También puede habilitar el acceso DTC de red mediante la herramienta administrativa Servicios de componentes o mediante programación a través de la biblioteca de administración de COM+. Para obtener información sobre procedimientos, vea "Configuring DTC Security" (Configuración de la seguridad de DTC) en la Ayuda de administración de servicios de componentes.

**Para habilitar el acceso DTC de red**

1.  En el **menú** Inicio, seleccione **Panel de control** y, a continuación, seleccione Agregar o quitar **programas.**

2.  Haga **clic en Agregar o quitar Windows componentes**.

3.  Seleccione **Servidor de aplicaciones** y haga clic en **Detalles**.

4.  Active la casilla situada junto a **Habilitar el acceso DTC de** red y, a continuación, haga clic en **Aceptar.**

5.  Haga **clic en** Siguiente para completar el asistente Windows componentes.

6.  Haga **clic en** Finalizar para cerrar el asistente.

## <a name="pausing-and-disabling-applications"></a>Pausa y deshabilitación de aplicaciones

Las aplicaciones COM+ ahora son más fáciles de administrar. Un administrador puede pausar y reanudar aplicaciones de servidor COM+, deshabilitar y habilitar aplicaciones de servidor o biblioteca COM+, o incluso componentes configurados individuales. Las características de pausa y deshabilitación impiden futuras activaciones sin que ello afecte a las instancias de componentes existentes. Consulte "Administración de aplicaciones COM+" en la Ayuda de administración de servicios de componentes para obtener más información.

## <a name="process-dumping"></a>Volcado de proceso

No es fácil solucionar problemas de aplicaciones en un entorno de producción. ¿Cómo se recopila información sobre un problema sin alterar los procesos en ejecución? COM+ ahora proporciona una solución a través de su nueva característica de volcado de proceso. Esta característica permite al administrador del sistema volcar todo el estado de un proceso sin terminarlo. Consulte "Administración de la herramienta de volcado de procesos para depurar aplicaciones COM+" en la Ayuda de administración de servicios de componentes para obtener más información.

## <a name="process-initialization"></a>Inicialización de procesos

Muchas aplicaciones de servidor deben realizar una inicialización y limpieza específicas cuando se inician y se apagan. Al ejecutar en Windows Server 2003, puede crear una clase que implemente la [**interfaz IProcessInitializer.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) Cuando se inicia el proceso, llama a [**IProcessInitializer::Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) y, al cerrarlo, llama a [**IProcessInitializer::Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Esto ofrece al componente la oportunidad de realizar las tareas necesarias, como inicializar conexiones, archivos y cachés.

## <a name="running-com-applications-as-nt-services"></a>Ejecución de aplicaciones COM+ como servicios NT

Los desarrolladores de COM+ ahora pueden usar la herramienta administrativa Servicios de componentes para configurar e implementar una aplicación de servidor COM+ como servicio NT. Esto significa que el servidor se puede iniciar o reiniciar automáticamente si la aplicación siempre necesita estar en ejecución; que la aplicación COM+ puede ejecutarse como la cuenta del sistema local si necesita realizar operaciones con privilegios; y que los servicios dependientes de la aplicación ahora se pueden iniciar automáticamente. Consulte [Aplicaciones COM+ que se ejecutan como aplicaciones de servicio para](com--applications-running-as-service-applications.md) obtener información detallada.

## <a name="side-by-side-assemblies"></a>Ensamblados en paralelo

Los ensamblados en paralelo (SxS) permiten a las aplicaciones especificar qué versión de un archivo DLL del sistema o componente COM clásico usar, como MDAC, MFS, MSVCRT o MSXML. Por ejemplo, si una aplicación ASP se basa en MSXML versión 2.0, puede asegurarse de que esta aplicación sigue MSXML la versión 2.0 incluso después de aplicar Service Pack al servidor. Es decir, incluso cuando se instala una nueva versión de MSXML en el equipo, la versión 2.0 permanece y la aplicación la usa.

Para configurar ensamblados SxS, debe conocer la ruta de acceso al archivo DLL y que el archivo de manifiesto COM+ existe en todos los directorios virtuales que necesiten usar el archivo DLL. El manifiesto COM+ es un archivo XML que tiene información sobre dónde está instalado un archivo DLL. El manifiesto se usa para crear un contexto de activación para la aplicación. Los contextos de activación permiten a una aplicación cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada. Puede usar la herramienta administrativa Servicios de componentes o la propiedad ApplicationDirectory para especificar la ruta de acceso completa del directorio raíz de la aplicación que contiene un archivo de manifiesto de ensamblado SxS válido. Para obtener más información, [vea Aplicaciones aisladas y ensamblados en paralelo.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

## <a name="windows-error-reporting"></a>Informe de errores de Windows

COM+ 1.5 incluye compatibilidad con el componente Informe de errores de Windows (WER), disponible a partir de Windows XP. WER permite a los usuarios notificar a Microsoft los errores de la aplicación, los errores de kernel y las aplicaciones que no responden. Estas notificaciones permiten a los equipos de soporte al cliente de Microsoft resolver problemas técnicos de forma más eficaz. Además, el componente Informe de errores de Windows permite a los desarrolladores de COM+ recibir información que se puede usar para mejorar sus aplicaciones. Para obtener más información, consulta [Informe de errores de Windows](/windows/desktop/wer/windows-error-reporting).

 

 
