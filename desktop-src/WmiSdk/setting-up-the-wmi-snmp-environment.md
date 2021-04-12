---
description: La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI. La información de este tema explica cómo configurar el entorno de WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configuración del entorno SNMP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361444"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configuración del entorno SNMP de WMI

La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI. La información de este tema explica cómo configurar el entorno de WMI SNMP.

En este tema se describen las siguientes secciones:

## <a name="installing-the-snmp-provider"></a>Instalación del proveedor SNMP

El servicio SNMP no está habilitado de forma predeterminada. Puede habilitar el servicio SNMP y el proveedor SNMP de WMI a través del panel de control. Tenga en cuenta que el servicio SNMP debe estar habilitado y en ejecución para que el proveedor SNMP de WMI funcione.

A partir de Windows Vista, use el siguiente procedimiento para instalar el proveedor SNMP.

**Para instalar el proveedor SNMP**

1.  En el **Panel de control**, seleccione **programas**.
2.  En **programas y características**, seleccione **activar o desactivar las características de Windows**.
3.  En la lista características de Windows, desplácese hacia abajo hasta la **característica SNMP** y expanda la lista para que pueda ver el **proveedor SNMP de WMI**.
4.  Active la casilla correspondiente al **proveedor SNMP de WMI**. La casilla de la **característica SNMP** se selecciona automáticamente porque el proveedor requiere SNMP.
5.  Haga clic en **OK**.
6.  En un símbolo del sistema o en el menú **Inicio** , ejecute Services. msc y asegúrese de que se ha iniciado el servicio SNMP.

## <a name="creating-an-snmp-namespace"></a>Crear un espacio de nombres SNMP

Un espacio de nombres SNMP define una vista de un dispositivo de red.

> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

En el procedimiento siguiente se describe cómo crear un [*espacio de nombres*](gloss-n.md)WMI de SNMP.

**Para crear un espacio de nombres SNMP**

1.  Cree una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) mediante la compilación de un archivo [*Managed Object Format*](gloss-m.md) . mof o mediante la [API com para WMI](com-api-for-wmi.md).

    Para obtener más información, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).

2.  Asocie los [*calificadores*](gloss-q.md) de proveedor SNMP con la definición de espacio de nombres.

    Los calificadores de proveedor SNMP contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP obtiene acceso a un dispositivo SNMP. Para obtener más información, consulte [**calificadores específicos del proveedor SNMP**](qualifiers-specific-to-the-snmp-provider.md).

3.  Use la herramienta de línea de comandos [MOFCOMP](mofcomp.md) para cargar el código MOF en el repositorio WMI.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

En el siguiente ejemplo de código MOF \\ se define el espacio de nombres SNMP con un subconjunto de los calificadores que se pueden asociar a un espacio de nombres SNMP.

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a>Inserción de datos MIB SNMP en WMI

Como proveedor, el proveedor SNMP actúa como un puente entre los datos SNMP y las clases WMI. Por lo tanto, debe tener clases en WMI que representen distintos aspectos de un dispositivo habilitado para SNMP. Para ello, debe usar el compilador de módulos de información SNMP ([smi2smir](smi2smir.md)) para compilar la información de administración de SNMP desde el formato SNMP en las definiciones de esquema CIM equivalentes. A continuación, puede dirigir la salida del compilador de información a una base de datos de esquema SNMP denominada "repositorio de información de módulos SNMP (SMIR)" o a varios tipos diferentes de archivos MOF.

El compilador se ejecuta en el modo de línea de comandos, utilizando un archivo MIB como entrada. El siguiente comando carga el archivo MIB especificado en SMIR.

**smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configuración de comunidades SNMP

Como medida de seguridad, la comunidad SNMP "pública" no se crea de forma predeterminada. Puede crear la comunidad como se describe en [configuración del registro de comunidades](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Si no tiene ninguna comunidad, cree la comunidad "pública" para tener acceso al proveedor SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Generación de archivos MOF a partir de archivos MIB

Los siguientes comandos son un ejemplo de cómo generar archivos MOF a partir de los archivos MIB que se instalan cuando se instala el proveedor SNMP.

**CD** *% WINDIR% \\ system32 \\ WBEM \\ SNMP*

**Smi2smir/g** *... \\ . \\ hostmib. MIB* **>** *hostmib. mof*

**Smi2smir/g** *... \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*

**Smi2smir/g** *... \\ . \\ NIPX. MIB* **>** *NIPX. mof*

**Smi2smir/g** *... \\ . \\ MIB \_ II. MIB* II. **>** *\_ MOF*

**Smi2smir/g** *... \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*

**Smi2smir/g** *... \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*

**Smi2smir/g** *... \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*

**Smi2smir/g** *... \\ . \\ wfospf. MIB* **>** *wfospf. mof*

**Smi2smir/g** *... \\ . \\ DHCP. MIB \\ . \\ ... msft. MIB* **>** *DHCP. mof*

**Smi2smir/g** *... \\ . \\ WINS. MIB \\ .. \\ .. msft. MIB* **>** *gana. mof*

**Smi2smir/g** *... \\ . \\ mipx. MIB \\ .. \\ .. msft. MIB* **>** *mipx. mof*

**Smi2smir/g** *... \\ . \\ mripsap. MIB \\ .. \\ .. msft. MIB* **>** *mripsap. mof*

**Smi2smir/g** *... \\ . \\ msipbtp. MIB \\ .. \\ .. msft. MIB* **>** *msipbtp. mof*

**Smi2smir/g** *... \\ . \\ msiprip2. MIB \\ .. \\ .. msft. MIB* **>** *msiprip2. mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Agregar archivos MOF de SNMP al repositorio WMI

Los siguientes comandos son un ejemplo de cómo agregar los archivos MOF que se generan desde los archivos MIB al repositorio WMI. Si desea agregar los archivos MOF a la lista de archivos que se van a restaurar automáticamente en una recuperación del [*repositorio WMI*](gloss-w.md) , agregue el marcador **-Autorrecuperación** al final de cada comando. Para obtener más información acerca de la herramienta de línea de comandos de WMI Mofcomp.exe, consulte [**MOFCOMP**](mofcomp.md).

**MOFCOMP** *hostmib. mof*

**MOFCOMP** *ipforwd. mof*

**MOFCOMP** *NIPX. mof*

 *MIB \_ II. mof* de MOFCOMP

**MOFCOMP** *lmmib2. mof*

**MOFCOMP** *mcastmib. mof*

**MOFCOMP** *rfc2571. mof*

**MOFCOMP** *wfospf. mof*

**MOFCOMP** *DHCP. mof*

**MOFCOMP** *mipx. mof*

**MOFCOMP** *mripsap. mof*

**MOFCOMP** *msipbtp. mof*

**MOFCOMP** *msiprip2. mof*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
