---
description: Un proveedor es un objeto de Modelo de objetos componentes (COM) que actúa como intermediario entre WMI y un objeto administrado.
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: Desarrollar un proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9249c251f75f08f9e5142e70a507b0dced8f91df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575356"
---
# <a name="developing-a-wmi-provider"></a>Desarrollar un proveedor WMI

Un proveedor es un objeto de Modelo de objetos componentes (COM) que actúa como intermediario entre WMI y un objeto administrado. Por ejemplo, cuando una aplicación o script solicita datos de disco mediante la clase [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de WMI, los datos se obtienen dinámicamente a través del proveedor [win32 preinstalado.](/windows/desktop/CIMWin32Prov/win32-provider)

Si desea proporcionar datos a través de WMI a otras aplicaciones, puede crear un proveedor de código no administrado escribiendo un servidor COM o a través de los **asistentes ATL de WMI** en Visual Studio. Puede escribir un proveedor de código administrado mediante WMI en el .NET Framework. En los temas de esta sección se describe el proceso de escritura de un proveedor COM no administrado.

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el repositorio [*WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) en el archivo Managed Object Format (MOF).

 

Un proveedor consta de clases definidas en el esquema [*Managed Object Format (MOF)*](gloss-m.md) y un archivo DLL que lleva a cabo las funciones del proveedor. Por ejemplo, el MOF que define las clases del proveedor Win32 es CIMWin32.mof y el archivo DLL es CIMWin32.dll, ambos se encuentran en %windir% \\ System32 \\ Wbem.

El esquema MOF para el proveedor puede contener varios tipos de proveedor. Por ejemplo, el proveedor [del registro de](/previous-versions/windows/desktop/eventlogprov/event-log-provider) eventos tiene tipos de proveedor de eventos, métodos y instancias en un archivo MOF denominado Ntevt.mof. Se recomienda ensamblar todas las clases y el esquema de registro de los proveedores relacionados en un archivo, en lugar de crear un archivo por clase.

Además de usar proveedores preinstalados, puede crear su propio proveedor para proporcionar información sobre un dispositivo de hardware o las operaciones de software.

En la tabla siguiente se enumeran las tareas básicas que crean un proveedor.



| Tarea                                                                                                                                                            | Descripción                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)                                                              | Desarrolle un modelo para las entidades que desea administrar a través de WMI y cree un archivo Managed Object Format (MOF) para describir el esquema.<br/> |
| [Proporcionar datos a WMI mediante la escritura de un proveedor](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | Cree el proveedor más básico que esté acoplado a WMI.<br/>                                                                                |
| [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md)                                                                    | Incluya el proveedor como componente dentro de una aplicación si no se ejecuta todo el tiempo.<br/>                                         |
| [Registro de un proveedor](registering-a-provider.md)                                                                                                            | Registre el proveedor con COM y WMI.<br/>                                                                                               |
| [Inicialización de un proveedor](initializing-a-provider.md)                                                                                                          | Implemente [**las interfaces IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemProviderInitSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)<br/>   |
| [Realizar llamadas a WMI](making-calls-to-wmi.md)                                                                                                                  | Llame a interfaces WMI desde un proveedor.<br/>                                                                                                  |
| [Suplantación de un cliente](impersonating-a-client.md)                                                                                                            | Establezca la seguridad para acceder a una aplicación cliente.<br/>                                                                                          |
| [Actualizar un proveedor](updating-a-provider.md)                                                                                                                  | Mejore el proveedor según sea necesario.<br/>                                                                                                       |
| [Descargar un proveedor](unloading-a-provider.md)                                                                                                                | Quite el proveedor de la memoria durante el apagado o cuando el proveedor esté inactivo.<br/>                                                         |
| [Proveedores de depuración y](debugging-providers.md) [clases de configuración y solución de problemas de proveedores](provider-configuration-and-troubleshooting-classes.md) | Depure el proveedor mediante las instalaciones proporcionadas por WMI.<br/>                                                                                 |
| [Obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | Evalúe si necesita un proveedor de compatibilidad de aplicaciones de 32 bits o si el proveedor de 64 bits puede proporcionar datos a ambos clientes.<br/>      |



 

En los temas siguientes se tratan los pasos necesarios para escribir diferentes tipos de proveedores:

-   [Escribir un proveedor de instancias](writing-an-instance-provider.md)
-   [Escribir un proveedor de métodos](writing-a-method-provider.md)
-   [Escribir un proveedor de eventos](writing-an-event-provider.md)
-   [Escribir un proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)
-   [Escribir un proveedor de clases](writing-a-class-provider.md)
-   [Escribir un proveedor de propiedades](writing-a-property-provider.md)
-   [Convertir un proveedor de instancias en un High-Performance de recursos](making-an-instance-provider-into-a-high-performance-provider.md)

 

