---
description: Puede usar la API del modelo de objetos componentes (COM) WMI para escribir aplicaciones cliente de administración o crear un nuevo proveedor de WMI.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706765"
---
# <a name="com-api-for-wmi"></a>API COM para WMI

Puede usar la API del modelo de objetos componentes (COM) WMI para escribir aplicaciones cliente de administración o crear un nuevo [*proveedor*](gloss-p.md)de WMI. La referencia de la API COM proporciona información para los administradores avanzados del sistema, así como para los desarrolladores que escriben aplicaciones de cliente y de proveedor.

Para obtener más información sobre cómo escribir aplicaciones de administración de la empresa de WMI, vea [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md). Para obtener más información sobre cómo escribir un proveedor WMI, vea [proporcionar datos a WMI](providing-data-to-wmi.md).

> [!Note]  
> WMI solo admite el desarrollo de C++ mediante Microsoft Visual C++ versión 6,0 y los sistemas de desarrollo posteriores. Sin embargo, también puede usar otros compiladores como los de Borland y Watcom.

 

Cada uno de los distintos objetos WMI hereda de una interfaz heredada en última instancia de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . COM determina el modo en que los implementadores de objetos, o interfaces, administran tareas como la administración de memoria, la administración de parámetros y el multithreading. Al ser compatible con COM, la API de COM para WMI garantiza que admita la funcionalidad proporcionada por las interfaces de cada objeto WMI.

Se tiene acceso a WMI a través de las siguientes interfaces COM específicas de WMI.



| Interfaz                                                                    | Descripción                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Enumerador que funciona con objetos de tipo [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject). Es similar a los enumeradores COM estándar, como [**IEnumVariant**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Implementado por Mofd.dll, esta interfaz proporciona una interfaz COM utilizada por el compilador MOF y cualquier otra aplicación que compile archivos MOF.                                                                                                                                                       |
| [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Se usa para simplificar el proceso de realizar llamadas asincrónicas desde un proceso de cliente.                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Realiza una copia de seguridad y restaura el contenido del repositorio WMI.                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Se usa para llamadas [semisincrónicas](making-a-semisynchronous-call-with-c--.md) de la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Al realizar estas llamadas, el método **IWbemServices** llamado se devuelve inmediatamente, junto con un objeto [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | Realiza el seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Contiene y manipula las definiciones de clase y las instancias de objeto de clase. Los desarrolladores no necesitan implementar esta interfaz; WMI proporciona su implementación.                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Lo utiliza el código de cliente para agregar o quitar enumeradores, objetos y actualizadores anidados en un actualizador.                                                                                                                                                                                                         |
| [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | Opcionalmente, se usa para comunicar información de contexto adicional a los proveedores cuando se envían llamadas [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) a la administración de Windows.                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Registra proveedores desacoplados con WMI.                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Asocia proveedores desacoplados a WMI. Esta interfaz permite a un proveedor hospedado en un proceso definir la duración de interoperabilidad de la interfaz y coexistir con otros proveedores.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Proporciona la interfaz principal para un proveedor de consumidor de eventos. A través de esta interfaz y el método [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) , un proveedor de consumidores de eventos puede indicar qué consumidores de eventos deben recibir un evento determinado.                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Se utiliza para iniciar la comunicación con un proveedor de eventos.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Implementado opcionalmente por proveedores de eventos que quieren saber qué tipos de filtros de consulta de eventos están activos actualmente para optimizar el rendimiento.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Implementado opcionalmente por proveedores de eventos que desean restringir el acceso del consumidor a su evento.                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | Inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas. Esta interfaz extiende [**IWbemObjectSink**](iwbemobjectsink.md), lo que proporciona nuevos métodos que se ocupan de la seguridad y el rendimiento.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Permite a los proveedores proporcionar objetos y enumeradores actualizables.                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Se utiliza en las operaciones de actualización para proporcionar un acceso rápido a las enumeraciones de objetos de instancia.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Obtiene el puntero de espacio de nombres inicial a la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para WMI en un equipo host específico.                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Proporciona acceso a los métodos y propiedades de un objeto. Un objeto [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) es un contenedor para una instancia actualizada por un [*actualizador.*](gloss-r.md)                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | Se utiliza para recibir los resultados de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y determinados tipos de notificaciones de eventos.                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Se usa para traducir instancias de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) a y desde distintos formatos de texto.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Admite la recuperación y actualización de propiedades individuales en una instancia de una clase WMI.                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Implementado por un proveedor de eventos si el proveedor se registra a sí mismo usando más de un **nombre** (varias instancias de [**\_ \_ Win32Provider**](--win32provider.md)) con el mismo valor de [CLSID](../com/clsid.md) . La clase proporciona un mecanismo para distinguir el proveedor con nombre que se debe usar. |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Se usa para inicializar los proveedores.                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Implementado por WMI y llamado por los proveedores para informar del estado de inicialización.                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Actúa como un contenedor para todo el conjunto de calificadores con nombre para una sola propiedad o un objeto completo (una clase o instancia).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Proporciona un punto de entrada a través del cual se puede analizar una consulta de [*lenguaje de consulta de WMI*](gloss-w.md) (WQL).                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Proporciona un punto de entrada a través del cual se pueden actualizar objetos actualizables como enumeradores o objetos actualizados.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Lo usan los clientes y proveedores para tener acceso a los servicios WMI. La interfaz solo se implementa mediante WMI y es la interfaz WMI principal.                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Extrae las descripciones de cadena de texto de los códigos de error o el nombre del subsistema en el que se produjo el error.                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Implementado por todos los consumidores de eventos lógicos. Es una interfaz receptora simple que acepta la entrega de objetos de evento.                                                                                                                                                                                          |



 

> [!Note]  
> Muchas de las funciones COM de WMI devuelven códigos de error numéricos que se documentan como constantes con nombre. Estas constantes se definen en Wbemcli. h en la carpeta de inclusión de WMI de PSDK \\ . Para obtener más información, vea [códigos de retorno de WMI](wmi-return-codes.md).

 

Para obtener más información acerca de los temas siguientes para la programación COM, vea [desarrollo de componentes]( /previous-versions//ee663263(v=vs.85)):

-   Interfaces y diseño de objetos.
-   Implementación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Administración de memoria
-   Controlar el recuento de referencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
