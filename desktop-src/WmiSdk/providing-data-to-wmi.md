---
description: WMI hace que los datos sobre los objetos administrables de Windows estén disponibles a través de los proveedores de WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Proporcionar datos a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811413"
---
# <a name="providing-data-to-wmi"></a>Proporcionar datos a WMI

WMI hace que los datos sobre los objetos administrables de Windows estén disponibles a través de los [*proveedores*](gloss-p.md)de WMI. Un proveedor recupera los datos de un componente del sistema, como un proceso, o una aplicación instrumentada, como SNMP o IIS, y pasa los datos a través de WMI a una aplicación de administración. Por ejemplo, cuando una aplicación o un script solicitan información del proceso mediante la clase de [**\_ proceso**](/windows/desktop/CIMWin32Prov/win32-process) de WMI Win32, los datos se obtienen dinámicamente a través de un proveedor preinstalado.

En este tema se describen las siguientes secciones:

-   [Crear un modelo para un objeto administrable](#creating-a-model-for-a-manageable-object)
-   [Implementar un modelo para un objeto administrable](#implementing-a-model-for-a-manageable-object)
-   [Determinar el tipo de proveedor que se va a implementar](#determining-a-provider-type-to-implement)
-   [Determinar un modelo de hospedaje (implementación) para un proveedor](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementar un proveedor](#implementing-a-provider)
-   [Registro de un proveedor con WMI y el sistema](#registering-a-provider-with-wmi-and-the-system)
-   [Probar un proveedor](#testing-a-provider)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Crear un modelo para un objeto administrable

Antes de desarrollar un proveedor, cree un modelo de datos para representar el objeto administrable que se va a exponer a través de WMI. Planea qué objetos de datos expondrá el proveedor. Por ejemplo, si planea administrar la resolución de pantalla del fondo de escritorio, debe decidir cómo modelar el escritorio en un archivo [*Managed Object Format (MOF)*](gloss-m.md) .

Para crear un modelo útil:

-   Determinar escenarios reales y modelar la información que un cliente puede querer leer y actualizar (por ejemplo, cambiar la imagen de fondo) de cada objeto administrable. Estas son las propiedades de clase.
-   Determine qué tipo de acciones puede realizar un cliente con cada objeto administrable. Estos son los métodos.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementar un modelo para un objeto administrable

Para implementar un modelo para objetos administrables, cree un archivo MOF que contenga una clase WMI que represente cada objeto. Para obtener más información acerca de la creación de un archivo MOF para definir clases WMI, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md). El registro del proveedor y sus clases normalmente se incluyen en el archivo MOF, aunque es posible usar la [API com](com-api-for-wmi.md) para crear clases y métodos. Para obtener más información, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el [*repositorio WMI*](gloss-w.md) si WMI tiene un error y se reinician, use la instrucción de preprocesador [**\# pragma autocover**](pragma-autorecover.md) en el archivo [*Managed Object Format (MOF)*](gloss-m.md) .

 

Después de crear el archivo MOF, compílelo con la herramienta [**Mofcomp.exe**](mofcomp.md) . De esta forma, se le notifican los errores en el archivo MOF y se agrega la clase WMI definida en el archivo MOF al [*repositorio WMI*](gloss-w.md) para que un proveedor pueda utilizar la clase.

## <a name="determining-a-provider-type-to-implement"></a>Determinar el tipo de proveedor que se va a implementar

WMI admite cierto número de tipos de proveedor, que determina la naturaleza de la información entregada y las operaciones admitidas por los proveedores.

Los tipos de proveedor son:

-   [*Proveedor de instancias*](gloss-i.md)
-   [*Proveedor de método*](gloss-m.md)
-   [*Proveedor de propiedades*](gloss-p.md)
-   Proveedor de clases
-   [*Proveedor de eventos*](gloss-e.md)
-   [*Proveedor de consumidor de eventos*](gloss-e.md)
-   [*Proveedor de asociación*](gloss-a.md)

La gran mayoría de los proveedores son proveedores de instancias y proveedores de métodos. Un proveedor de instancias es el proveedor más común y proporciona las instancias de una clase determinada. Un proveedor de métodos implementa los métodos de una o más clases. Para obtener más información sobre los tipos de proveedores, vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinar un modelo de hospedaje (implementación) para un proveedor

Los proveedores WMI son archivos binarios que se implementan como objetos COM. Esto significa que cada proveedor tiene un archivo DLL que se puede ejecutar en un proceso específico y en un contexto de seguridad. Esto es lo que WMI hace referencia como [*modelo de hospedaje*](gloss-h.md). WMI ofrece varias maneras de hospedar proveedores, pero el enfoque más común consiste en usar el modelo de proveedor acoplado (que se ejecuta en el proceso WMI) en el contexto de seguridad NetworkServiceHost. Un proveedor WMI se puede clasificar como acoplado o [*desacoplado*](gloss-d.md).

El término acoplado o el proveedor desacoplado determina en qué proceso de host se ejecuta el proveedor con respecto al proceso de WMIPRVSE.EXE proporcionado por WMI. Un procedimiento recomendado es determinar si los datos de administración que expone el proveedor y la API o la aplicación en la que se basa están siempre disponibles en el sistema o no. Si la API o la aplicación en la que se basa el proveedor siempre están disponibles (en ejecución en el sistema), el proveedor debe ser un proveedor acoplado, de lo contrario, debe ser un proveedor desacoplado. Para obtener más información sobre los modelos de hospedaje, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

Para obtener más información acerca de cómo crear un proveedor acoplado, consulte [proporcionar datos a WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md)y para obtener información sobre cómo incorporar un proveedor desacoplado en una aplicación, consulte [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

Los proveedores acoplados se pueden describir como in-Process (en proceso) o fuera de proceso (fuera de proceso). Cuando un proveedor acoplado es un proveedor en proceso, se ejecuta bajo un proceso de hospedaje de WMI WMIPRVSE.EXE compartido y se implementa como un servidor en proceso COM (. dll). Cuando un proveedor es un proveedor fuera de proceso, WMI lo inicia a petición de un cliente o evento, pero se ejecuta como un proceso separado y se implementa como un archivo ejecutable (. exe).

## <a name="implementing-a-provider"></a>Implementar un proveedor

Un proveedor se puede implementar de las siguientes maneras:

-   Usar el Asistente para ATL en Visual Studio.

    El Asistente para ATL genera código de proveedor que implementa un proveedor acoplado. Al utilizar el Asistente para ATL, puede especificar que desea crear un modelo en tiempo de ejecución del proveedor (. dll) o fuera de proceso (. exe).

-   Definir un objeto COM que contenga el proveedor.

    El código del proveedor está escrito en C++. Para obtener más información, consulte [proporcionar datos a WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md).

-   Usar las clases del espacio de nombres [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) en el .NET Framework para crear un proveedor mediante código administrado. (Ya no se admite el espacio de nombres **System. Management. Instrumentation** ).

    Este proceso crea un proveedor desacoplado.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registro de un proveedor con WMI y el sistema

Antes de utilizar el proveedor de un consumidor, es importante registrarlo con el sistema WMI y el subsistema COM de Windows.

Un archivo MOF puede contener varios tipos de proveedores para las mismas clases. El mismo nombre de proveedor se registra como, por ejemplo, una instancia de o un proveedor de métodos. Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).

## <a name="testing-a-provider"></a>Probar un proveedor

Cuando se registra el código del proveedor, es importante probar correctamente el proveedor mediante el proveedor de distintos consumidores (por ejemplo, scripts, código administrado de .NET y consumidores de C++).

Realice las tareas siguientes para probar el proveedor:

-   Asegúrese de que el proveedor se carga correctamente mediante el seguimiento de las notificaciones de eventos de [**msft \_ WmiProvider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) . Estos eventos le informarán sobre cualquier error de carga del proveedor. Otras clases de solución de problemas que pueden resultar útiles son [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) y [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace). Para obtener más información sobre los proveedores de solución de problemas, vea [depuración de proveedores](debugging-providers.md) y [clases de solución de problemas](provider-configuration-and-troubleshooting-classes.md).
-   Si el proveedor es un proveedor de instancia o método, asegúrese de probar cada funcionalidad del proveedor una por una para evitar confusiones al seguir la lógica del código.
-   Para un proveedor de instancias, cree una aplicación cliente o un script que invoque cada interfaz del proveedor (enumeración, get, Put y Delete). Incluso si no se supone que el proveedor implemente nada, debe devolver un mensaje "no compatible". Puede encontrar los valores devueltos que ya se han definido en los [códigos de retorno de WMI](wmi-return-codes.md).
-   Para asegurarse de que el contexto de seguridad deseado funciona según lo previsto, invoque las operaciones admitidas por el proveedor desde un contexto de seguridad que no sea de administrador. El proveedor debe admitir la suplantación. Si un usuario que carece de las credenciales de seguridad correctas intenta actualizar los datos o realizar una operación que ejecuta un método, el proveedor debe denegar el acceso con el mensaje de error correspondiente.
-   Para obtener más información sobre la seguridad del proveedor, consulte [protección del proveedor](securing-your-provider.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedaje y seguridad de proveedores](provider-hosting-and-security.md)
</dt> <dt>

[Proporcionar datos a WMI escribiendo un proveedor](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrar un proveedor](registering-a-provider.md)
</dt> <dt>

[Solución de problemas de aplicaciones cliente WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Obtener y proporcionar datos en una plataforma de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
