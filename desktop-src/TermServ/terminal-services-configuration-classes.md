---
title: Servicios de Escritorio remoto Configuration
description: El proveedor WMI Servicios de Escritorio remoto configuration proporciona las siguientes clases. A continuación se muestra una ilustración.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000135"
---
# <a name="remote-desktop-services-configuration-classes"></a>Servicios de Escritorio remoto Configuration

El proveedor WMI Servicios de Escritorio remoto configuration proporciona las siguientes clases. A continuación se muestra una ilustración.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dd>

Representa la asociación entre los elementos administrados del sistema y la clase de configuración definida para ellos.

</dd> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> <dd>

Clase base para todos los componentes del sistema que representan componentes abstractos del sistema, como perfiles, procesos o funcionalidades del sistema, en forma de dispositivos lógicos.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Clase base para la jerarquía de elementos del sistema.

</dd> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dd>

Representa parámetros operativos y relacionados con la configuración para uno o varios elementos del sistema administrados.

</dd> <dt>

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> <dd>

representa un terminal.

</dd> <dt>

[**TerminalError de Win32 \_**](win32-terminalerror.md)
</dt> <dd>

Representa un error de terminal.

</dd> <dt>

[**TerminalService de Win32 \_**](win32-terminalservice.md)
</dt> <dd>

una subclase de la [**clase De \_ servicio Win32.**](/windows/desktop/CIMWin32Prov/win32-service) [**Win32 \_ TerminalService**](win32-terminalservice.md) representa la **propiedad Element** de la [**asociación \_ TerminalServiceToSetting de Win32.**](win32-terminalservicetosetting.md)

</dd> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> <dd>

representa la configuración de un Escritorio remoto host de sesión de escritorio remoto.

</dd> <dt>

[**Terminal De \_ Win32ServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

representa la asociación entre una instancia de la clase [**\_ TerminalService de Win32**](win32-terminalservice.md) y el valor de una determinada propiedad [**\_ TerminalServiceSetting de Win32.**](win32-terminalservicesetting.md)

</dd> <dt>

[**Terminal \_ Win32Setting**](win32-terminalsetting.md)
</dt> <dd>

representa la configuración que se puede aplicar a un terminal.

</dd> <dt>

[**Terminal \_ Win32TerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

representa la asociación entre un terminal y sus opciones de configuración.

</dd> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> <dd>

permite la eliminación de una cuenta que existe en el [**Terminal Win32 \_ y**](win32-terminal.md) la modificación de los permisos existentes.

</dd> <dt>

[**TSClientSetting de Win32 \_**](win32-tsclientsetting.md)
</dt> <dd>

define los valores de configuración de la [**clase \_ Terminal Win32**](win32-terminal.md) relacionada con la directiva de conexión.

</dd> <dt>

[**TSDiscoveredLicenseServer de Win32 \_**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.

</dd> <dt>

[**\_TSEnvironmentSetting de Win32**](win32-tsenvironmentsetting.md)
</dt> <dd>

define los valores de configuración de la clase [**\_ Terminal Win32,**](win32-terminal.md) incluida la directiva de programa inicial.

</dd> <dt>

[**\_TSGeneralSetting de Win32**](win32-tsgeneralsetting.md)
</dt> <dd>

representa la configuración general del terminal, como el nivel de cifrado y el protocolo de transporte.

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

define los valores de configuración para la [**clase \_ Terminal Win32**](win32-terminal.md) relacionada con el inicio de sesión de cliente.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

enumera la lista de adaptadores de red que se pueden configurar para un [**\_ terminal Win32,**](win32-terminal.md)según el protocolo de terminal y el método de transporte especificados.

</dd> <dt>

[**\_TSNetworkAdapterSetting de Win32**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

define varias opciones de configuración para la [**clase \_ Terminal Win32,**](win32-terminal.md) incluidas las propiedades relacionadas con el adaptador de red y el número máximo de conexiones permitidas.

</dd> <dt>

[**\_TSPermissionsSetting de Win32**](win32-tspermissionssetting.md)
</dt> <dd>

incluye un método para agregar nuevas cuentas al terminal y un método para restaurar los permisos predeterminados en un terminal.

</dd> <dt>

[**TSRemoteControlSetting de Win32 \_**](win32-tsremotecontrolsetting.md)
</dt> <dd>

define los valores de configuración de control remoto para la [**clase \_ Terminal Win32.**](win32-terminal.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Define la configuración Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) para la clase [**\_ TSSessionDirectorySetting de Win32.**](win32-tssessiondirectorysetting.md)

</dd> <dt>

[**\_TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Representa la asociación entre una instancia de la [**clase \_ TerminalService win32**](win32-terminalservice.md) y una instancia de la [**clase \_ TSSessionDirectory de Win32.**](win32-tssessiondirectory.md)

</dd> <dt>

[**TSSessionSetting de Win32 \_**](win32-tssessionsetting.md)
</dt> <dd>

define los valores de configuración de la [**clase \_ Terminal Win32,**](win32-terminal.md) como los límites de tiempo y las acciones de desconexión y reconexión.

</dd> <dt>

[**TSVirtualIP de Win32 \_**](win32-tsvirtualip.md)
</dt> <dd>

Define la configuración de virtualización del protocolo de Internet (IP) para un servidor host de sesión de Escritorio remoto.

</dd> <dt>

[**\_TSVirtualIPSetting de Win32**](win32-tsvirtualipsetting.md)
</dt> <dd>

Representa la asociación entre una clase de elemento [**\_ TerminalService de Win32**](win32-terminalservice.md) y una clase de [**configuración \_ TSVirtualIP de Win32.**](win32-tsvirtualip.md)

</dd> </dl>

En la ilustración siguiente se muestran las relaciones entre estas clases.

![las relaciones entre las clases admitidas](images/tswmi.png)

 

 