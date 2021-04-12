---
title: Servicios de Escritorio remoto clases de configuración
description: El proveedor WMI de configuración de Servicios de Escritorio remoto proporciona las siguientes clases. A continuación se muestra una ilustración.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420759"
---
# <a name="remote-desktop-services-configuration-classes"></a>Servicios de Escritorio remoto clases de configuración

El proveedor WMI de configuración de Servicios de Escritorio remoto proporciona las siguientes clases. A continuación se muestra una ilustración.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

Representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.

</dd> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dd>

La clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.

</dd> <dt>

[**ManagedSystemElement de CIM \_**](cim-managedsystemelement.md)
</dt> <dd>

La clase base para la jerarquía de elementos del sistema.

</dd> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dd>

Representa los parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.

</dd> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dd>

representa un terminal.

</dd> <dt>

[**Win32 \_ TerminalError**](win32-terminalerror.md)
</dt> <dd>

Representa un error de terminal.

</dd> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dd>

una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) . [**Win32 \_ TerminalService**](win32-terminalservice.md) representa la propiedad de **elemento** de la Asociación [**\_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .

</dd> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dd>

representa la configuración de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

</dd> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

representa la asociación entre una instancia de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) y el valor de una propiedad [**\_ TerminalServiceSetting de Win32**](win32-terminalservicesetting.md) determinada.

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

representa la configuración que se puede aplicar a un terminal.

</dd> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

representa la asociación entre un terminal y sus valores de configuración.

</dd> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> <dd>

permite la eliminación de una cuenta que existe en [**el \_ terminal Win32**](win32-terminal.md) y la modificación de los permisos existentes.

</dd> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> <dd>

define la configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con la Directiva de conexión.

</dd> <dt>

[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.

</dd> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluida la Directiva de programa inicial.

</dd> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dd>

representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

define la configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con el inicio de sesión de cliente.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

enumera la lista de adaptadores de red que se pueden configurar para un [**\_ terminal Win32**](win32-terminal.md), según el protocolo de terminal y el método de transporte especificados.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

define diversos valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluidas las propiedades relacionadas con el adaptador de red y el número máximo de conexiones permitidas.

</dd> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> <dd>

incluye un método para agregar cuentas nuevas al terminal y un método para restaurar los permisos predeterminados en un terminal.

</dd> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> <dd>

define la configuración de control remoto para la clase de [**\_ terminal Win32**](win32-terminal.md) .

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Define los valores de configuración del agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) para la clase [**\_ TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md) .

</dd> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Representa la asociación entre una instancia de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) y una instancia de la clase [**\_ TSSessionDirectory de Win32**](win32-tssessiondirectory.md) .

</dd> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> <dd>

define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , como los límites de tiempo, y las acciones de desconexión y reconexión.

</dd> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> <dd>

Define la configuración de virtualización del Protocolo de Internet (IP) para un servidor host de sesión de escritorio remoto.

</dd> <dt>

[**Win32 \_ TSVirtualIPSetting**](win32-tsvirtualipsetting.md)
</dt> <dd>

Representa la asociación entre una clase de elemento de [**Win32 \_ TerminalService**](win32-terminalservice.md) y una clase de configuración [**\_ TSVirtualIP de Win32**](win32-tsvirtualip.md) .

</dd> </dl>

En la ilustración siguiente se muestran las relaciones entre estas clases.

![las relaciones entre las clases admitidas](images/tswmi.png)

 

 