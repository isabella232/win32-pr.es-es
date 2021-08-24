---
title: Implementar un proveedor de Client-Side (proxy) Automatización de la interfaz de usuario cliente
description: En este tema se describe cómo escribir un proveedor de proxy para un control no compatible y agregarlo a la lista de servidores proxy usados por las aplicaciones cliente.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Automatización de la interfaz de usuario implementación del proveedor del lado cliente
- Automatización de la interfaz de usuario,implementación del proveedor
- Automatización de la interfaz de usuario, implementar proveedores del lado cliente
- Automatización de la interfaz de usuario, proveedores de implementación
- Automatización de la interfaz de usuario,proxies
- proxies
- proveedores del lado cliente
- providers,implementing
- implementar proveedores del lado cliente
- implementar proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8724f0761b5d7e5d361742734901990136a7a98c1b2f541b4fadb69c31a92d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861305"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementar un proveedor de Client-Side (proxy) Automatización de la interfaz de usuario cliente

Microsoft Automatización de la interfaz de usuario proporciona un conjunto de servidores proxy para la mayoría de los controles estándar, como los que se usan en aplicaciones de Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF). Sin embargo, muchos controles personalizados y controles de terceros no implementan proveedores Automatización de la interfaz de usuario nativos. Para que puedan acceder Automatización de la interfaz de usuario aplicaciones cliente, estos controles deben estar equipados con proveedores del lado cliente, también conocidos como proveedores *de proxy* o *servidores proxy.*

En este tema se describe cómo escribir un proveedor de proxy para un control no compatible y agregarlo a la lista de servidores proxy usados por las aplicaciones cliente. Contiene los temas siguientes:

-   [¿Qué es un proxy?](#what-is-a-proxy)
-   [¿Qué es una factoría de proxy?](#what-is-a-proxy-factory)
-   [Asignación de factoría de proxy](#proxy-factory-mapping)
-   [Administración de servidores proxy predeterminados](#managing-default-proxies)
-   [Temas relacionados](#related-topics)

Para obtener ejemplos de código que muestran cómo implementar proveedores de proxy, vea Temas de [Automatización de la interfaz de usuario proveedores.](uiauto-howto-topics-for-uiautomation-providers.md)

## <a name="what-is-a-proxy"></a>¿Qué es un proxy?

Un proveedor del lado cliente, o proxy, es un objeto que implementa la interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) en nombre de un control que no tiene una implementación **de IRawElementProviderSimple** propia. Sin un proxy, este control es en gran medida opaco para Automatización de la interfaz de usuario, que solo puede proporcionar información básica disponible desde el identificador de ventana **(HWND),** como la ubicación del control.

## <a name="what-is-a-proxy-factory"></a>¿Qué es una factoría de proxy?

Cada proxy requiere un *generador de proxy correspondiente,* que es un objeto que expone la [**interfaz IUIAutomationProxyFactory.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) Automatización de la interfaz de usuario mantiene una tabla interna de entradas de generador de *proxy,* cada una de las cuales contiene una referencia al generador de proxy para cada proxy y un conjunto de condiciones. Cuando Automatización de la interfaz de usuario encuentra un control que no tiene una implementación nativa de [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) busca una entrada de generador de proxy cuyas condiciones indican que admite el control. Automatización de la interfaz de usuario busca en la tabla desde el principio y, cuando encuentra una entrada que coincida, Automatización de la interfaz de usuario llama al método [**IUIAutomationProxyFactory::CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) del generador. Si el proxy correspondiente se crea correctamente, el Automatización de la interfaz de usuario deja de buscar y usa el objeto de proxy recién creado; De lo contrario, Automatización de la interfaz de usuario búsqueda continua.

Una aplicación cliente crea una instancia de una entrada de generador de proxy mediante el método [**IUIAutomation::CreateProxyFactoryEntry,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) que devuelve un puntero de interfaz [**IUIAutomationProxyFactoryEntry.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) Los clientes usan métodos expuestos por **IUIAutomationProxyFactoryEntry para** especificar el conjunto de condiciones que usa el generador de proxy para crear el proxy.

Cuando llama a [**IUIAutomationProxyFactory::CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider), Automatización de la interfaz de usuario pasa los parámetros que el objeto de generador de proxy puede usar para determinar si el proxy admite adecuadamente el control personalizado. Si es así, el generador de proxy crea una instancia del proxy y devuelve el puntero de interfaz [**IRawElementProviderSimple;**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) de lo contrario, devuelve un **puntero NULL.**

## <a name="proxy-factory-mapping"></a>Asignación de factoría de proxy

De forma predeterminada, Automatización de la interfaz de usuario busca en la tabla de generador de proxy en el orden siguiente.



| Pedido | Proxy                        | Descripción                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: proxy sin control | Para ventanas con el nombre de clase exacto o el nombre de clase base "ComboBoxEx32".         |
| 2     | Microsoft: proxy sin control | Para ventanas con el nombre de clase exacto o el nombre de clase base "WorkerW".              |
| 3     | Microsoft: proxy sin control | Para ventanas con el nombre de clase exacto o el nombre de clase base "SHELLDLL \_ DefView".    |
| 4     | Microsoft: Proxy de contenedor   | Para ventanas con el nombre de clase exacto o el nombre de clase base " \# 32770".              |
| 5     | Microsoft: Proxy de contenedor   | Para ventanas con un nombre de clase o un nombre de clase base que contenga "AfxControlBar".     |
| 6     | Microsoft: TreeView Proxy    | Para ventanas con un nombre de clase o un nombre de clase base que contenga "SysTreeView32".     |
| 7     | Microsoft: ListView Proxy    | Para ventanas con un nombre de clase o un nombre de clase base que contenga "SysListView32" (1). |
| 8     | Microsoft: ListView Proxy    | Para ventanas con un nombre de clase o un nombre de clase base que contenga "SysListView32" (2). |
| 9     | Microsoft: MSAA Proxy        | Para cualquier ventana.                                                                  |



 

Los servidores proxy 7 y 8 son entradas duplicadas para el control SysListView32. Sin modificaciones, el proxy 7 siempre se usa para el control SysListView32 y el proxy 8 nunca se usa. El proxy 8 solo se usa para los elementos de lista visibles y normalmente lo usan las aplicaciones cliente que solo funcionan con elementos visibles o que tienen requisitos de rendimiento estrictos. Estos clientes pueden quitar el proxy 7.

El proxy 9, el Microsoft Active Accessibility para Automatización de la interfaz de usuario proxy, siempre debe ser la última entrada de la tabla. Esto permite Microsoft Active Accessibility de reserva para los controles que implementan Microsoft Active Accessibility, pero no Automatización de la interfaz de usuario.

Al modificar las entradas de la tabla de generador de proxy, debe evaluar cuidadosamente la nueva posición de las entradas. Se recomienda colocar las entradas de los servidores proxy personalizados después de los servidores proxy que no son de control y de contenedor, pero antes de Microsoft Active Accessibility para Automatización de la interfaz de usuario proxy. Además, aunque es posible hacer que el código en la llamada a [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) determine si debe admitir un identificador de ventana determinado **(HWND),** es más eficaz permitir que Automatización de la interfaz de usuario seleccione el proxy en función del nombre de clase y mantener el código condicional en el **método CreateProvider** al mínimo.

Automatización de la interfaz de usuario mantiene una tabla de generador de proxy independiente para cada cliente. Cuando un cliente cambia su tabla de proxy, los cambios afectan solo al propio cliente; otros clientes no se ven afectados.

## <a name="managing-default-proxies"></a>Administración de servidores proxy predeterminados

Cuando una aplicación cliente crea el objeto [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) la tabla de generador de proxy contiene inicialmente entradas solo para los proveedores de proxy predeterminados para los controles estándar. Mediante la [**interfaz IUIAutomationProxyFactoryMapping,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) los clientes pueden agregar nuevas entradas, quitar entradas no deseadas, cambiar el orden de las entradas, y así sucesivamente. Un cliente puede recuperar un puntero de interfaz **IUIAutomationProxyFactoryMapping** llamando al método [**IUIAutomation::P roxyFactoryMapping.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping)

La tabla de servidores proxy disponibles contiene una [**interfaz IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para cada proxy. Cada **IUIAutomationProxyFactoryEntry** especifica [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) y la clase de control a la que sirve el proxy, y define cómo se deben controlar los eventos.

La tabla de servidores proxy se representa mediante una interfaz [**IUIAutomationProxyFactoryMapping,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) que se puede obtener de la propiedad [**IUIAutomation::P roxyFactoryMapping.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) Una aplicación puede usar **métodos IUIAutomationProxyFactoryMapping** para agregar y eliminar servidores proxy. Para crear una nueva entrada para agregarla a esta tabla, use [**IUIAutomation::CreateProxyFactoryEntry para**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) obtener la interfaz y, a continuación, use los métodos [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para definir la clase de control aplicable y el comportamiento del proxy.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un proveedor de Client-Side (proxy Automatización de la interfaz de usuario)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Automatización de la interfaz de usuario del programador del proveedor de aplicaciones](uiauto-providerportal.md)
</dt> </dl>

 

 