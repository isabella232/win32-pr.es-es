---
title: Implementar un proveedor de automatización de la interfaz de usuario de Client-Side (proxy)
description: En este tema se describe cómo escribir un proveedor proxy para un control no compatible y agregarlo a la lista de servidores proxy utilizados por las aplicaciones cliente.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Automatización de la interfaz de usuario, implementación del proveedor del lado cliente
- Automatización de la interfaz de usuario, implementación del proveedor
- Automatización de la interfaz de usuario, implementar proveedores del lado cliente
- Automatización de la interfaz de usuario, implementar proveedores
- Automatización de la interfaz de usuario, servidores proxy
- proxies
- proveedores del lado cliente
- proveedores, implementar
- implementación de proveedores del lado cliente
- implementar proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2bdb4a94ba6e693792508de5c573317299b0d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077840"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementar un proveedor de automatización de la interfaz de usuario de Client-Side (proxy)

La automatización de la interfaz de usuario de Microsoft proporciona un conjunto de servidores proxy para la mayoría de los controles estándar, como los que se usan en las aplicaciones de Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF). Sin embargo, muchos controles personalizados y controles de terceros no implementan proveedores de automatización de la interfaz de usuario nativa. Para que las aplicaciones cliente de automatización de la interfaz de usuario puedan acceder a ellos, estos controles deben proporcionarse con proveedores del lado cliente, también conocidos como *proveedores proxy* o *servidores* proxy.

En este tema se describe cómo escribir un proveedor proxy para un control no compatible y agregarlo a la lista de servidores proxy utilizados por las aplicaciones cliente. Contiene los temas siguientes:

-   [¿Qué es un proxy?](#what-is-a-proxy)
-   [¿Qué es un generador de proxy?](#what-is-a-proxy-factory)
-   [Asignación de generador de proxy](#proxy-factory-mapping)
-   [Administración de servidores proxy predeterminados](#managing-default-proxies)
-   [Temas relacionados](#related-topics)

Para ver ejemplos de código que muestran cómo implementar proveedores de proxy, consulte los [temas de procedimientos para los proveedores de automatización de la interfaz de usuario](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>¿Qué es un proxy?

Un proveedor del lado cliente, o proxy, es un objeto que implementa la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en nombre de un control que no tiene una implementación de **IRawElementProviderSimple** propia. Sin un proxy, este tipo de control es principalmente opaco a la automatización de la interfaz de usuario, que puede proporcionar solo información básica disponible en el identificador de ventana (**hWnd**), como la ubicación del control.

## <a name="what-is-a-proxy-factory"></a>¿Qué es un generador de proxy?

Cada proxy requiere un *generador de proxy* correspondiente, que es un objeto que expone la interfaz [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) . La automatización de la interfaz de usuario mantiene una tabla interna de entradas de la *factoría de proxy*, cada una de las cuales contiene una referencia al generador de proxy para cada proxy y un conjunto de condiciones. Cuando la automatización de la interfaz de usuario encuentra un control que no tiene una implementación de [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) nativa, busca una entrada de generador de proxy cuyas condiciones indican que es compatible con el control. La automatización de la interfaz de usuario busca en la tabla desde el principio y, cuando encuentra una entrada coincidente, la automatización de la interfaz de usuario llama al método [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) del generador. Si el proxy coincidente se crea correctamente, la automatización de la interfaz de usuario deja de buscar y utiliza el objeto proxy recién creado; de lo contrario, la automatización de la interfaz de usuario continúa buscando.

Una aplicación cliente crea una instancia de una entrada de generador de proxy mediante el método [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) , que devuelve un puntero de interfaz [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Los clientes usan métodos expuestos por **IUIAutomationProxyFactoryEntry** para especificar el conjunto de condiciones que usa el generador de proxy para crear el proxy.

Cuando llama a [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider), la automatización de la interfaz de usuario pasa los parámetros que el objeto de generador de proxy puede usar para determinar si el proxy admite adecuadamente el control personalizado. Si es así, el generador de proxy crea una instancia del proxy y devuelve el puntero de interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ; de lo contrario, devuelve un puntero **nulo** .

## <a name="proxy-factory-mapping"></a>Asignación de generador de proxy

De forma predeterminada, la automatización de la interfaz de usuario busca en la tabla del generador de proxy en el siguiente orden.



| Pedido | Proxy                        | Descripción                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: proxy sin control | Para Windows con el nombre de clase exacto o el nombre de clase base "ComboBoxEx32".         |
| 2     | Microsoft: proxy sin control | Para Windows con el nombre de clase exacto o el nombre de clase base "WorkerW".              |
| 3     | Microsoft: proxy sin control | Para Windows con el nombre de clase exacto o el nombre de clase base "SHELLDLL \_ DefView".    |
| 4     | Microsoft: proxy de contenedor   | Para Windows con el nombre de clase exacto o el nombre de clase base " \# 32770".              |
| 5     | Microsoft: proxy de contenedor   | Para Windows con un nombre de clase o nombre de clase base que contiene "AfxControlBar".     |
| 6     | Microsoft: proxy de TreeView    | Para Windows con un nombre de clase o nombre de clase base que contiene "SysTreeView32".     |
| 7     | Microsoft: proxy de ListView    | Para Windows con un nombre de clase o nombre de clase base que contiene "SysListView32" (1). |
| 8     | Microsoft: proxy de ListView    | Para Windows con un nombre de clase o nombre de clase base que contiene "SysListView32" (2). |
| 9     | Microsoft: proxy de MSAA        | Para cualquier ventana.                                                                  |



 

Los proxies 7 y 8 son entradas duplicadas para el control SysListView32. Sin modificaciones, el proxy 7 siempre se usa para el control SysListView32 y el proxy 8 nunca se usa. El proxy 8 solo se usa para los elementos de lista visibles y normalmente lo usan las aplicaciones cliente que solo funcionan con elementos visibles, o que tienen requisitos de rendimiento estrictos. Estos clientes pueden quitar el proxy 7.

Proxy 9, Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario, siempre debe ser la última entrada de la tabla. Esto habilita la funcionalidad de reserva de Microsoft Active Accessibility para los controles que implementan Microsoft Active Accessibility, pero no para la automatización de la interfaz de usuario.

Al modificar entradas en la tabla del generador de proxy, debe evaluar cuidadosamente la nueva posición de las entradas. Se recomienda colocar las entradas para los proxies personalizados después de los proxies de contenedor y sin control, pero antes de que Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario. Además, aunque es posible que el código de la llamada a [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) determine si debe admitir un identificador de ventana determinado (**hWnd**), es más eficaz permitir que la automatización de la interfaz de usuario seleccione el proxy basándose en el nombre de clase y mantener un código condicional en el método **CreateProvider** como mínimo.

La automatización de la interfaz de usuario mantiene una tabla de generador de proxy independiente para cada cliente. Cuando un cliente cambia su tabla de proxy, los cambios solo afectan al propio cliente; otros clientes no se ven afectados.

## <a name="managing-default-proxies"></a>Administración de servidores proxy predeterminados

Cuando una aplicación cliente crea el objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , la tabla de generador de proxy contiene inicialmente entradas solo para los proveedores de proxy predeterminados para los controles estándar. Mediante el uso de la interfaz [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , los clientes pueden agregar nuevas entradas, quitar entradas no deseadas, cambiar el orden de las entradas, etc. Un cliente puede recuperar un puntero de la interfaz **IUIAutomationProxyFactoryMapping** llamando al método [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) .

La tabla de servidores proxy disponibles contiene una interfaz [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para cada proxy. Cada **IUIAutomationProxyFactoryEntry** especifica el [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) y la clase de control a los que el proxy atiende, y define cómo se deben controlar los eventos.

La tabla de servidores proxy se representa mediante una interfaz [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , que se puede obtener a partir de la propiedad [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) . Una aplicación puede usar métodos **IUIAutomationProxyFactoryMapping** para agregar y eliminar servidores proxy. Para crear una nueva entrada para agregarla a esta tabla, use [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) para obtener la interfaz y, a continuación, use los métodos [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para definir la clase de control aplicable y el comportamiento del proxy.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un proveedor de automatización de la interfaz de usuario de Client-Side (proxy)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Guía del programador del proveedor de UI Automation](uiauto-providerportal.md)
</dt> </dl>

 

 