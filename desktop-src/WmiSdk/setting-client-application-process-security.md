---
description: Las aplicaciones cliente que llaman a interfaces WMI pueden controlar los niveles de seguridad de sus procesos.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Establecer la seguridad del proceso de la aplicación cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bfa0a42390ffa433cff01300b0976d40553665c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073061"
---
# <a name="setting-client-application-process-security"></a>Establecer la seguridad del proceso de la aplicación cliente

Las aplicaciones cliente que llaman a interfaces WMI pueden controlar los niveles de seguridad de sus procesos. Todas las aplicaciones WMI acceden a WMI a través de COM y puede llamar a la función COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de los procesos. Las aplicaciones que hacen llamadas asincrónicas a WMI y las aplicaciones que se registran como consumidores de eventos establecen niveles de seguridad en la llamada a WMI.

Si no realiza una llamada explícita a [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)COM la llama implícitamente con valores del Registro. Sin embargo, los valores del Registro pueden tener una configuración inferior para la suplantación y autenticación que no proporcionan la seguridad necesaria para WMI. Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante C++.](setting-the-default-process-security-level-using-c-.md)

No se recomienda el acceso asincrónico a WMI. Una devolución de llamada asincrónica permite a un usuario no autenticado proporcionar datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincronosa o sincrónica o realice comprobaciones de acceso adecuadas en la aplicación cliente. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Las llamadas a cualquiera de los servidores proxy wmi [**(IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) [**IEnumWbemClassObject,**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)o [**IWbemRefresher)**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)usan un puntero fuera de proceso. Para obtener más información sobre los valores predeterminados y las recomendaciones, vea Establecer la seguridad [en IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

En el procedimiento siguiente se describen los pasos que debe realizar para establecer la seguridad de WMI en el proceso de aplicación.

**Para establecer la seguridad de WMI en el proceso de aplicación**

1.  Determine los niveles de seguridad necesarios para los Windows operativos en los que se ejecuta la aplicación cliente.
2.  Llame a la función COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad predeterminada para el proceso en el que se ejecuta la aplicación cliente. Esto declara la cantidad de seguridad que requieren otras aplicaciones para acceder al proceso en el que se ejecuta la aplicación.
3.  Si necesita cambiar la seguridad en un proxy individual, por ejemplo, en otra llamada a [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)llame a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Si necesita controlar el hardware remoto o un objeto del sistema que requiere más privilegios, use la función [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar los privilegios necesarios. Tenga en cuenta que no se puede habilitar un privilegio que el proceso aún no tiene asignado. Para obtener más información, vea [Comprobar el acceso a objetos privados.](/windows/desktop/SecAuthZ/checking-access-to-private-objects)

Para obtener más información sobre cómo establecer el nivel de seguridad de proceso predeterminado, vea Establecer el nivel de seguridad de proceso predeterminado mediante [C++](setting-the-default-process-security-level-using-c-.md) y Establecer el nivel de seguridad de proceso [predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
