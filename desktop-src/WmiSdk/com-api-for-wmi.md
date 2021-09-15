---
description: Puede usar la API modelo de objetos componentes (COM) de WMI para escribir aplicaciones cliente de administración o crear un nuevo proveedor WMI.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465903"
---
# <a name="com-api-for-wmi"></a>API COM para WMI

Puede usar la API modelo de objetos componentes (COM) de WMI para escribir aplicaciones cliente de administración o crear un nuevo [*proveedor*](gloss-p.md)WMI. La referencia de api COM proporciona información para administradores avanzados del sistema, así como para desarrolladores que escriben aplicaciones cliente y proveedor.

Para obtener más información sobre cómo escribir aplicaciones de administración empresarial wmi, vea [Crear una aplicación WMI mediante C++.](creating-a-wmi-application-using-c-.md) Para obtener más información sobre cómo escribir un proveedor WMI, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

> [!Note]  
> WMI solo admite el desarrollo de C++ Microsoft Visual C++ versión 6.0 y posteriores. Sin embargo, también puede usar otros compiladores, como los de Borland y Suchcom.

 

Cada uno de los distintos objetos WMI hereda de una interfaz heredada en última instancia de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) COM determina cómo los implementadores de objetos, o interfaces, controlan tareas como la administración de memoria, la administración de parámetros y el multithreading. Al cumplir con COM, la API COM para WMI garantiza que admite la funcionalidad proporcionada por las interfaces de cada objeto WMI.

Se tiene acceso a WMI a través de las siguientes interfaces COM específicas de WMI.



| Interfaz                                                                    | Descripción                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Enumerador que funciona con objetos de tipo [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject). Es similar a los enumeradores COM estándar, como [**IEnumVariant.**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Implementada por Mofd.dll, esta interfaz proporciona una interfaz COM que usa el compilador MOF y cualquier otra aplicación que compile archivos MOF.                                                                                                                                                       |
| [**IUnsecuredChev**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Se usa para simplificar el proceso de realizar llamadas asincrónicas desde un proceso de cliente.                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Hace una copia de seguridad y restaura el contenido del repositorio WMI.                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Se usa [para las llamadas semisincronosas](making-a-semisynchronous-call-with-c--.md) de [**la interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Al realizar estas llamadas, el método **llamado IWbemServices** devuelve inmediatamente, junto con un [**objeto IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | Realiza un seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Contiene y manipula definiciones de clase e instancias de objeto de clase. Los desarrolladores no necesitan implementar esta interfaz. WMI proporciona su implementación.                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Lo usa el código de cliente para agregar o quitar enumeradores, objetos y actualizadores anidados en un actualizador.                                                                                                                                                                                                         |
| [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | Opcionalmente se usa para comunicar información de contexto adicional a los proveedores al enviar [**llamadas IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) a Windows Management.                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Registra proveedores desacoplados con WMI.                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Asocia proveedores desacoplados a WMI. Esta interfaz permite a un proveedor hospedado en procesos definir la duración de interoperabilidad de la interfaz y coexistir con otros proveedores.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Proporciona la interfaz principal para un proveedor de consumidores de eventos. A través de esta interfaz y [**el método FindConsumer,**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) un proveedor de consumidores de eventos puede indicar qué consumidores de eventos deben recibir un evento determinado.                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Se usa para iniciar la comunicación con un proveedor de eventos.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Opcionalmente, los proveedores de eventos que desean saber qué tipos de filtros de consulta de eventos están activos actualmente para optimizar el rendimiento.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Opcionalmente, los proveedores de eventos que desean restringir el acceso de los consumidores a su evento.                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | Inicia la comunicación con un proveedor de eventos mediante un conjunto restringido de consultas. Esta interfaz amplía [**IWbemObjectSink,**](iwbemobjectsink.md)lo que proporciona nuevos métodos que se ocupa de la seguridad y el rendimiento.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Permite a los proveedores proporcionar objetos actualizables y enumeradores.                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Se usa en las operaciones de actualización para proporcionar acceso rápido a enumeraciones de objetos de instancia.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Obtiene el puntero de espacio de nombres inicial a [**la interfaz IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para WMI en un equipo host específico.                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Proporciona acceso a los métodos y propiedades de un objeto . Un [**objeto IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) es un contenedor para una instancia actualizada por [*un actualizador*](gloss-r.md).                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | Se usa para recibir los resultados de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y determinados tipos de notificaciones de eventos.                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Se usa para traducir [**instancias de IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) a y desde distintos formatos de texto.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Admite la recuperación y actualización de propiedades individuales en una instancia de una clase WMI.                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Implementado por un proveedor de eventos si el proveedor se registra con más de un **nombre** (varias instancias de [**\_ \_ Win32Provider)**](--win32provider.md)con el mismo [valor CLSID.](../com/clsid.md) La clase proporciona un mecanismo para distinguir qué proveedor con nombre se debe usar. |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Se usa para inicializar proveedores.                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Implementado por WMI y llamado por los proveedores para notificar el estado de inicialización.                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Actúa como contenedor para todo el conjunto de calificadores con nombre para una sola propiedad o un objeto completo (una clase o instancia).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Proporciona un punto de entrada a través [*del cual se lenguaje de consulta de WMI*](gloss-w.md) consulta de lenguaje de consulta de WMI (WQL).                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Proporciona un punto de entrada a través del cual se pueden actualizar objetos actualizables, como enumeradores o objetos de actualizador.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Usado por clientes y proveedores para acceder a los servicios WMI. La interfaz solo se implementa mediante WMI y es la interfaz WMI principal.                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Extrae descripciones de cadenas de texto de códigos de error o el nombre del subsistema donde se produjo el error.                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Implementado por todos los consumidores de eventos lógicos. Es una interfaz de receptor simple que acepta la entrega de objetos de evento.                                                                                                                                                                                          |



 

> [!Note]  
> Muchas de las funciones COM de WMI devuelven códigos de error numéricos que se documentan como constantes con nombre. Estas constantes se definen en Wbemcli.h en la carpeta PSDK WMI \\ Include. Para obtener más información, vea [Códigos de retorno WMI.](wmi-return-codes.md)

 

Para obtener más información sobre los temas siguientes para la programación COM, vea [Desarrollo de componentes]( /previous-versions//ee663263(v=vs.85)):

-   Interfaces y diseño de objetos.
-   Implementar [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Administración de memoria
-   Control del recuento de referencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
