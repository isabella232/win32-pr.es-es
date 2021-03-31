---
description: La versión 1,5 de COM+ agrega nuevas características diseñadas para aumentar la escalabilidad, la disponibilidad y la capacidad de administración generales de las aplicaciones COM+ tanto para desarrolladores como para administradores del sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novedades de COM+ 1,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994237002ea5d19c2cb00364f1064df38ed7271f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423439"
---
# <a name="whats-new-in-com-15"></a>Novedades de COM+ 1,5

La versión 1,5 de COM+ agrega nuevas características diseñadas para aumentar la escalabilidad, la disponibilidad y la capacidad de administración generales de las aplicaciones COM+ tanto para desarrolladores como para administradores del sistema.

COM+ 1,5 está disponible a partir de Windows XP y Windows Server 2003. Las nuevas características de COM+ 1,5 no están disponibles en Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level las comprobaciones de acceso habilitadas de forma predeterminada

Como parte de la seguridad mejorada del sistema, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. En versiones anteriores, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente. A partir de Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Vea [crear una nueva aplicación com+](creating-a-new-com--application.md), [habilitar las comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)y [habilitar las comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md) para obtener más información y procedimientos sobre cómo cambiar la configuración predeterminada.

## <a name="application-pooling"></a>Agrupación de aplicaciones

Con la nueva propiedad ConcurrentApps del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) en la colección de [**aplicaciones**](applications.md) , la agrupación de aplicaciones com+ agrega escalabilidad para los procesos de un solo subproceso y se integra con el nuevo servicio de reciclaje de aplicaciones com+. Consulte [agrupación de aplicaciones com+](com--application-pooling.md) para obtener información detallada.

## <a name="application-recycling"></a>Reciclaje de aplicaciones

El reciclaje de aplicaciones aumenta significativamente la estabilidad general de las aplicaciones. Dado que el rendimiento de la mayoría de las aplicaciones puede reducirse con el tiempo debido a factores como pérdidas de memoria, la dependencia del código de terceros y el uso de recursos no escalables, el reciclaje de aplicaciones COM+ proporciona una solución sencilla para cerrar correctamente un proceso asociado a una aplicación y reiniciarlo. Consulte [reciclaje de aplicaciones com+](com--application-recycling.md) para obtener información detallada. Vea también "configurar el reciclaje de procesos" en la ayuda de administración de servicios de componentes para obtener un procedimiento paso a paso para configurar el reciclaje de procesos.

## <a name="com-partitions"></a>Particiones COM+

En esta versión, COM+ incorpora compatibilidad para las particiones COM+, una característica que permite instalar y configurar varias versiones de aplicaciones COM+ en el mismo equipo. Esta característica puede ahorrarle el costo y el esfuerzo que conlleva el uso de varios servidores para administrar diferentes versiones de una aplicación. En un único equipo, cada partición actúa como un servidor virtual. Después de instalar la aplicación en cada partición, se crean conjuntos de particiones que asignan usuarios a los servidores lógicos. Vea [particiones com+](com--partitions.md) para obtener información detallada acerca de cómo configurar y administrar particiones de com+. Vea también "Administrar particiones de aplicación" en la ayuda de administración de servicios de componentes para obtener procedimientos paso a paso.

## <a name="com-services-without-components"></a>Servicios COM+ sin componentes

Con COM+ 1,5, puede usar los servicios proporcionados por COM+ sin necesidad de generar un componente que contenga los métodos que llaman a esos servicios. Esto beneficia a los desarrolladores que normalmente no usan componentes, sino que desean usar servicios COM+ como transacciones o el seguimiento de COM+. Mediante el uso de servicios COM+ sin componentes, los desarrolladores pueden evitar la sobrecarga que supone crear un componente que se usa para tener acceso únicamente a los servicios COM+ que necesitan. Consulte [servicios com+ sin componentes](com--services-without-components.md) para obtener información detallada.

## <a name="com-soap-service"></a>Servicio SOAP de COM+

Con COM+ 1,5, ahora puede exponer una aplicación COM+ como un servicio Web XML. También puede utilizar de forma transparente un servicio Web XML, tanto si se implementa mediante COM+ como si no, como un componente COM. Esto significa que puede crear fácilmente nuevos servicios Web XML a partir de las aplicaciones COM+ existentes e incorporar fácilmente servicios Web XML en nuevas aplicaciones COM+. Vea [servicio SOAP de com+](com--soap-service.md) para obtener información detallada.

## <a name="configurable-isolation-levels"></a>Niveles de aislamiento configurables

Los desarrolladores de COM+ pueden utilizar la nueva propiedad TxIsolationLevel o la herramienta administrativa Servicios de componentes para configurar el nivel de aislamiento de una aplicación según sea necesario, lo que ayuda a aumentar la simultaneidad, el rendimiento y la escalabilidad. Esta flexibilidad permite que los usuarios con la cantidad adecuada de experiencia obtengan todos los últimos onzas de rendimiento de sus aplicaciones. Consulte [configuración de niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md) para obtener información detallada.

## <a name="creating-private-components"></a>Crear componentes privados

En escenarios en los que hay varios componentes auxiliares en una aplicación que solo se pueden llamar desde otros componentes de esa aplicación, esta versión de COM+ le permite usar una nueva propiedad, IsPrivateComponent, para marcar estos componentes como privados. (En la versión anterior de COM+, todos los componentes debían ser públicos para tener acceso a los servicios COM+, lo que significa que estos componentes se podían activar desde otras aplicaciones). Un componente privado solo se puede ver y activar en otros componentes de la misma aplicación, lo que le ofrece más control sobre la funcionalidad que se debe exponer. Solo necesita documentar y mantener los componentes públicos, a la vez que hace uso de componentes privados a los que no se puede tener acceso desde fuera de la aplicación, pero que pueden seguir aprovechando todos los servicios COM+.

## <a name="dtc-security-settings"></a>Configuración de seguridad de DTC

Se han agregado varias nuevas configuraciones de seguridad para Microsoft Coordinador de transacciones distribuidas (DTC), lo que le permite personalizar los niveles de seguridad para administrar las transacciones distribuidas. Vea Consideraciones de seguridad de DTC sobre estas opciones de configuración y cómo implementarlas.

Para facilitar la autenticación mutua, el DTC está restringido a ejecutarse en la cuenta NetworkService. Consulte Administración de cuentas y privilegios para obtener información detallada.

Para la recuperación con bases de datos XA, se recomienda que se proporcione a la cuenta NetworkService los permisos y los roles necesarios para realizar esta recuperación. El método exacto para hacerlo es específico de cada base de datos. Vea deshabilitar transacciones distribuidas nativas y deshabilitar las transacciones TIP y XA para obtener más información.

Para ayudar a proporcionar un sistema más seguro al utilizar transacciones XA, las plataformas de Windows Server 2003 incluyen una nueva entrada del registro para especificar archivos DLL XA. Al actualizar a Windows Server 2003, puede trabajar con las transacciones XA como antes creando una entrada del registro en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MSDTC \\ XADLL**, donde el nombre de valor es el nombre del archivo DLL (en el formato *DllName*. dll) y el valor es la ruta de acceso completa del archivo dll. Debe crear una entrada para cada archivo DLL de XA en uso. Si el equipo que ejecuta DTC forma parte de un clúster, es necesario realizar la entrada del registro para cada nodo del clúster. Vea Administrar transacciones XA para obtener más información.

## <a name="low-memory-activation-gates"></a>Low-Memory las puertas de activación

Con esta versión, COM+ comprueba automáticamente la memoria antes de crear un servidor o un objeto COM+. Si el porcentaje de memoria virtual disponible para la aplicación cae por debajo de un umbral fijo, se produce un error en la activación antes de que se cree el objeto. Al producirse errores en estas activaciones que normalmente se ejecutarían, el servicio de las [puertas de activación de COM+ Low-Memory](com--low-memory-activation-gates.md) mejora en gran medida la confiabilidad del sistema.

## <a name="moving-and-copying-com-components"></a>Mover y copiar componentes COM

Con esta versión, COM+ le permite trasladar y copiar los componentes. Esto significa que puede configurar una única implementación física de un componente muchas veces diferentes. Obtiene la reutilización de componentes en un nivel binario en lugar de en el nivel de código fuente, lo que da como resultado menos código, menores costos de desarrollo y un tiempo de comercialización más rápido. Vea [mover componentes](moving-components.md) y [copiar componentes](copying-components.md) para obtener información detallada.

## <a name="network-access"></a>Acceso de red

El acceso de red COM+ está deshabilitado de forma predeterminada en Windows Server 2003, lo que significa que COM+ solo se puede usar de forma local de forma predeterminada. Use el procedimiento siguiente para habilitar el acceso de red COM+.

**Para habilitar el acceso de red COM+**

1.  En el menú **Inicio** , seleccione **Panel de control** y, a continuación, seleccione **Agregar o quitar programas**.

2.  Haga clic en **Agregar o quitar componentes de Windows**.

3.  Seleccione **Servidor de aplicaciones** y haga clic en **Detalles**.

4.  Active la casilla situada junto a **Habilitar el acceso de red com+** y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **siguiente** para completar el Asistente para componentes de Windows.

6.  Haga clic en **Finalizar** para cerrar el asistente.

El acceso a las transacciones de red DTC está deshabilitado de forma predeterminada en Windows Server 2003. En estas plataformas, el DTC solo puede realizar transacciones locales de forma predeterminada. Use el procedimiento siguiente para habilitar el acceso a DTC desde la red.

> [!NOTE]
> También puede habilitar el acceso a DTC desde la red mediante la herramienta administrativa Servicios de componentes o mediante programación a través de la biblioteca de administración de COM+. Para obtener información de procedimientos, vea "configuración de la seguridad de DTC" en la ayuda de administración de servicios de componentes.

**Para habilitar el acceso a DTC desde la red**

1.  En el menú **Inicio** , seleccione **Panel de control** y, a continuación, seleccione **Agregar o quitar programas**.

2.  Haga clic en **Agregar o quitar componentes de Windows**.

3.  Seleccione **Servidor de aplicaciones** y haga clic en **Detalles**.

4.  Active la casilla situada junto a **Habilitar el acceso de DTC** a la red y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **siguiente** para completar el Asistente para componentes de Windows.

6.  Haga clic en **Finalizar** para cerrar el asistente.

## <a name="pausing-and-disabling-applications"></a>Pausar y deshabilitar aplicaciones

Ahora, las aplicaciones COM+ son más fáciles de administrar. Un administrador puede pausar y reanudar las aplicaciones de servidor COM+, o bien deshabilitar y habilitar las aplicaciones de servidor o biblioteca COM+, o incluso componentes individuales configurados. Las características pausar y deshabilitar evitan futuras activaciones sin afectar a las instancias de componentes existentes. Vea "Administrar aplicaciones COM+" en la ayuda de administración de servicios de componentes para obtener más información.

## <a name="process-dumping"></a>Proceso de volcado

No es fácil solucionar problemas de las aplicaciones en un entorno de producción. ¿Cómo recopila información sobre un problema sin alterar los procesos en ejecución? COM+ proporciona ahora una solución a través de la nueva característica de volcado de memoria. Esta característica permite al administrador del sistema volcar todo el estado de un proceso sin terminarlo. Vea "administrar la herramienta de volcado de proceso para depurar aplicaciones COM+" en la ayuda de administración de servicios de componentes para obtener más información.

## <a name="process-initialization"></a>Inicialización del proceso

Muchas aplicaciones de servidor necesitan realizar una inicialización y limpieza específicas cuando se inician y se apagan. Cuando se ejecuta en Windows Server 2003, puede crear una clase que implemente la interfaz [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) . Cuando el proceso se inicia, llama a [**IProcessInitializer:: startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) y al cerrarse, llama a [**IProcessInitializer:: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Esto proporciona al componente la oportunidad de realizar las tareas necesarias, como inicializar conexiones, archivos y memorias caché.

## <a name="running-com-applications-as-nt-services"></a>Ejecutar aplicaciones COM+ como servicios NT

Los desarrolladores de COM+ ahora pueden usar la herramienta administrativa Servicios de componentes para configurar e implementar una aplicación de servidor COM+ como un servicio NT. Esto significa que el servidor puede iniciarse o reiniciarse automáticamente si la aplicación siempre debe estar en ejecución; que la aplicación COM+ pueda ejecutarse como la cuenta del sistema local si necesita realizar operaciones con privilegios; y que los servicios dependientes de la aplicación ahora se pueden iniciar automáticamente. Consulte [aplicaciones com+ que se ejecutan como aplicaciones de servicio](com--applications-running-as-service-applications.md) para obtener información detallada.

## <a name="side-by-side-assemblies"></a>Ensamblados en paralelo

Los ensamblados en paralelo (SxS) permiten a las aplicaciones especificar qué versión de un archivo DLL del sistema o componente COM clásico usar, como MDAC, MFS, MSVCRT o MSXML. Por ejemplo, si una aplicación ASP se basa en la versión 2,0 de MSXML, puede asegurarse de que esta aplicación siga usando MSXML versión 2,0 incluso después de aplicar los Service Packs al servidor. Es decir, incluso cuando se instala una nueva versión de MSXML en el equipo, la versión 2,0 permanece y se usa en la aplicación.

Para configurar ensamblados SxS, debe conocer la ruta de acceso a la DLL y que el archivo de manifiesto de COM+ exista en cada directorio virtual que necesite usar el archivo DLL. El manifiesto de COM+ es un archivo XML que contiene información sobre dónde se instala un archivo DLL. El manifiesto se usa para crear un contexto de activación para la aplicación. Los contextos de activación permiten a una aplicación cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada. Puede usar la herramienta administrativa Servicios de componentes o la propiedad ApplicationDirectory para especificar la ruta de acceso completa del directorio raíz de la aplicación que contiene un archivo de manifiesto de ensamblado SxS válido. Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Informe de errores de Windows

COM+ 1,5 incluye compatibilidad con el componente Informe de errores de Windows (WER), disponible a partir de Windows XP. WER permite a los usuarios notificar a Microsoft los errores de la aplicación, los errores del kernel y las aplicaciones que no responden. Estas notificaciones permiten a los equipos de soporte al cliente de Microsoft solucionar problemas técnicos de manera más eficaz. Además, el componente Informe de errores de Windows permite a los desarrolladores de COM+ recibir información que se puede usar para mejorar sus aplicaciones. Para obtener más información, consulta [Informe de errores de Windows](/windows/desktop/wer/windows-error-reporting).

 

 
