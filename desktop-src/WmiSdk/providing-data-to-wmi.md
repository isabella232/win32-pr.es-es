---
description: WMI hace que los datos Windows objetos administrables estén disponibles a través de proveedores WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Proporcionar datos a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22fbff46959c001f589587f21b8b2b50ab5c5187d387338f407bf45e3e1a29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316579"
---
# <a name="providing-data-to-wmi"></a>Proporcionar datos a WMI

WMI hace que los datos Windows objetos administrables estén disponibles a través de [*proveedores*](gloss-p.md)WMI. Un proveedor recupera datos de un componente del sistema, como un proceso, o una aplicación instrumentada, como SNMP o IIS, y pasa esos datos a través de WMI a una aplicación de administración. Por ejemplo, cuando una aplicación o script solicita información de proceso mediante la clase Process [**de WMI \_ Win32,**](/windows/desktop/CIMWin32Prov/win32-process) los datos se obtienen dinámicamente a través de un proveedor preinstalado.

En este tema se de abordan las siguientes secciones:

-   [Crear un modelo para un objeto administrable](#creating-a-model-for-a-manageable-object)
-   [Implementar un modelo para un objeto administrable](#implementing-a-model-for-a-manageable-object)
-   [Determinar un tipo de proveedor que se implementará](#determining-a-provider-type-to-implement)
-   [Determinar un modelo de hospedaje (implementación) para un proveedor](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementar un proveedor](#implementing-a-provider)
-   [Registro de un proveedor con WMI y el sistema](#registering-a-provider-with-wmi-and-the-system)
-   [Probar un proveedor](#testing-a-provider)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Crear un modelo para un objeto administrable

Antes de desarrollar un proveedor, cree un modelo de datos para representar el objeto administrable que se va a exponer a través de WMI. Planee qué objetos de datos expondrá el proveedor. Por ejemplo, si tiene previsto administrar la resolución de pantalla del fondo del escritorio, debe decidir cómo modelar el escritorio en un archivo [*Managed Object Format (MOF).*](gloss-m.md)

Para crear un modelo útil:

-   Determinar escenarios reales y modelar la información que un cliente puede querer leer y actualizar (por ejemplo, cambiar la imagen de fondo) para cada objeto administrable. Estas son las propiedades de la clase.
-   Determine qué tipo de acciones puede querer realizar un cliente con cada objeto administrable. Estos son los métodos.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementar un modelo para un objeto administrable

Para implementar un modelo para objetos administrables, cree un archivo MOF que contenga una clase WMI que represente cada objeto. Para obtener más información sobre cómo crear un archivo MOF para definir clases WMI, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md). El registro del proveedor y sus clases normalmente se incluye en el archivo MOF, aunque es posible usar la [API COM](com-api-for-wmi.md) para crear clases y métodos. Para obtener más información, vea [Desarrollar un proveedor WMI.](developing-a-wmi-provider.md)

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el repositorio [*WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) en el archivo [*Managed Object Format (MOF).*](gloss-m.md)

 

Después de crear el archivo MOF, compile el archivo [**mediante**](mofcomp.md)Mofcomp.exeherramienta. Esto le notifica errores en el archivo MOF y agrega la clase WMI definida en el archivo MOF al repositorio [*WMI*](gloss-w.md) para que un proveedor pueda usar la clase.

## <a name="determining-a-provider-type-to-implement"></a>Determinar un tipo de proveedor que se implementará

WMI admite un determinado número de tipos de proveedor, lo que determina la naturaleza de la información entregada y las operaciones admitidas por los proveedores.

Los tipos de proveedor son:

-   [*Proveedor de instancias*](gloss-i.md)
-   [*Proveedor de métodos*](gloss-m.md)
-   [*Proveedor de propiedades*](gloss-p.md)
-   Proveedor de clases
-   [*Proveedor de eventos*](gloss-e.md)
-   [*Proveedor de consumidores de eventos*](gloss-e.md)
-   [*Proveedor de asociación*](gloss-a.md)

La gran mayoría de los proveedores son proveedores de instancias y proveedores de métodos. Un proveedor de instancias es el proveedor más común y proporciona las instancias de una clase determinada. Un proveedor de métodos implementa los métodos de una o varias clases. Para obtener más información sobre los tipos de proveedores, vea [Developing a WMI Provider](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinar un modelo de hospedaje (implementación) para un proveedor

Los proveedores WMI son archivos binarios implementados como objetos COM. Esto significa que cada proveedor tiene un archivo DLL que se puede ejecutar dentro de un proceso y contexto de seguridad específicos. Esto es lo que WMI hace referencia a como el [*modelo de hospedaje*](gloss-h.md). WMI ofrece varias maneras de hospedar proveedores, pero el enfoque más común es usar el modelo de proveedor acoplado (que se ejecuta en el proceso WMI) en el contexto de seguridad NetworkServiceHost. Un proveedor WMI se puede clasificar como acoplado [*o desacoplado.*](gloss-d.md)

El término proveedor acoplado o desacoplado determina en qué proceso de host se ejecuta el proveedor con respecto al proceso de WMIPRVSE.EXE WMI proporcionado. Un procedimiento recomendado es determinar si los datos de administración que expone el proveedor y la API o aplicación en la que se basa siempre están disponibles en el sistema o no. Si la API o aplicación en la que se basa el proveedor siempre está disponible (ejecutándose en el sistema), el proveedor debe ser un proveedor acoplado, si no es así, debe ser un proveedor desacoplado. Para obtener más información sobre los modelos de hospedaje, vea [Provider Hosting and Security](provider-hosting-and-security.md).

Para obtener más información sobre cómo crear un proveedor acoplado, vea Proporcionar datos a [WMI](supplying-data-to-wmi-by-writing-a-provider.md)escribiendo un proveedor y, para obtener información sobre cómo incorporar un proveedor desacoplado en una aplicación, vea Incorporación de un proveedor en una [aplicación](incorporating-a-provider-in-an-application.md).

Los proveedores acoplados se pueden describir como en proceso (en proceso) o fuera de proceso (fuera de proceso). Cuando un proveedor acoplado es un proveedor en proceso, se ejecuta en un proceso de hospedaje de WMI de WMIPRVSE.EXE compartido y se implementa como un servidor en proceso COM (.dll). Cuando un proveedor es un proveedor fuera de proceso, WMI lo inicia a petición de un cliente o evento, pero se ejecuta como un proceso separado y se implementa como ejecutable (.exe).

## <a name="implementing-a-provider"></a>Implementar un proveedor

Un proveedor se puede implementar de las maneras siguientes:

-   Usar el Asistente ATL en Visual Studio.

    El Asistente atl genera código de proveedor que implementa un proveedor acoplado. Al usar el Asistente atl, puede especificar que desea crear un modelo en tiempo de ejecución de proveedor en proceso (.dll) o fuera de proceso (.exe).

-   Definir un objeto COM para que contenga el proveedor.

    El código del proveedor está escrito en C++. Para obtener más información, vea Proporcionar datos a [WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md).

-   El uso de las clases [**del espacio de nombres Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) .NET Framework para crear un proveedor mediante código administrado. (Ya no se admite el espacio de **nombres System.Management.Instrumentation).**

    Este proceso crea un proveedor desacoplado.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registro de un proveedor con WMI y el sistema

Antes de usar el proveedor de un consumidor, es importante registrarlo con el sistema WMI y el Windows COM.

Un archivo MOF puede contener varios tipos de proveedores para las mismas clases. El mismo nombre de proveedor se registra como, por ejemplo, una instancia o un proveedor de métodos. Para obtener más información, [vea Registrar un proveedor.](registering-a-provider.md)

## <a name="testing-a-provider"></a>Probar un proveedor

Cuando se registra el código del proveedor, es importante probar correctamente el proveedor mediante el proveedor de distintos consumidores (por ejemplo, scripts, código administrado de .NET y consumidores de C++).

Realice las siguientes tareas para probar el proveedor:

-   Asegúrese de que el proveedor se está cargando correctamente mediante el seguimiento de las notificaciones de [**eventos \_ MsfT WmiProvider \_ OperationEvent.**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) Estos eventos le informarán sobre los errores de carga del proveedor. Otras clases de solución de problemas que pueden resultar útiles [**son Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) y [**Win32 \_ ProcessStopTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) Para obtener más información sobre los proveedores de solución de problemas, vea [Proveedores de](debugging-providers.md) depuración y Configuración del proveedor y Clases de solución [de problemas](provider-configuration-and-troubleshooting-classes.md).
-   Si el proveedor es una instancia o un proveedor de métodos, asegúrese de probar cada funcionalidad del proveedor uno a uno para evitar confusiones al seguir la lógica del código.
-   Para un proveedor de instancias, cree una aplicación cliente o un script que invoque todas las interfaces del proveedor (enumeración, get, put y delete). Incluso si el proveedor no debe implementar nada, debe devolver un mensaje "no compatible". Puede encontrar los valores devueltos ya definidos en Códigos [de retorno wmi](wmi-return-codes.md).
-   Para asegurarse de que el contexto de seguridad deseado funciona según lo previsto, invoque las operaciones admitidas por el proveedor desde un contexto de seguridad no administrador. El proveedor debe admitir la suplantación. Si un usuario que carece de las credenciales de seguridad correctas intenta actualizar los datos o realizar una operación que ejecuta un método, el proveedor debe denegar el acceso con el mensaje de error adecuado.
-   Para obtener más información sobre la seguridad del proveedor, [vea Securing Your Provider](securing-your-provider.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedaje y seguridad del proveedor](provider-hosting-and-security.md)
</dt> <dt>

[Proporcionar datos a WMI mediante la escritura de un proveedor](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registro de un proveedor](registering-a-provider.md)
</dt> <dt>

[Solución de problemas de aplicaciones cliente WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Obtener y proporcionar datos en una plataforma de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
