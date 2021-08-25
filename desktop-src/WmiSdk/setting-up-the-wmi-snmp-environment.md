---
description: La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI. En la información de este tema se explica cómo configurar el entorno SNMP de WMI.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configuración del entorno SNMP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a090dab219c589fc8d9084c445e9a69c8d75afefb64400fe3029bfed66ab931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860434"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Configuración del entorno SNMP de WMI

La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI. En la información de este tema se explica cómo configurar el entorno SNMP de WMI.

En este tema se de abordan las siguientes secciones:

## <a name="installing-the-snmp-provider"></a>Instalación del proveedor SNMP

El servicio SNMP no está habilitado de forma predeterminada. Puede habilitar el servicio SNMP y el proveedor WMI SNMP a través del Panel de control. Tenga en cuenta que el servicio SNMP debe estar habilitado y en ejecución para que funcione el proveedor SNMP de WMI.

A partir Windows Vista, use el procedimiento siguiente para instalar el proveedor SNMP.

**Para instalar el proveedor SNMP**

1.  En la **Panel de control**, seleccione **Programas**.
2.  En **Programas y características,** **seleccione Activar o desactivar Windows características.**
3.  En la lista Windows características, desplácese hacia abajo hasta La característica **SNMP** y expanda la lista para que pueda ver el proveedor **SNMP de WMI.**
4.  Active la casilla del proveedor **SNMP de WMI.** La casilla de la **característica SNMP** se selecciona automáticamente porque el proveedor requiere SNMP.
5.  Haga clic en **Aceptar**.
6.  Desde un símbolo del sistema o el **menú** Inicio, ejecute Services.msc y asegúrese de que se ha iniciado el servicio SNMP.

## <a name="creating-an-snmp-namespace"></a>Creación de un espacio de nombres SNMP

Un espacio de nombres SNMP define una vista de un dispositivo de red.

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del sistema operativo [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

En el procedimiento siguiente se describe cómo crear un espacio de [*nombres*](gloss-n.md)WMI de SNMP.

**Para crear un espacio de nombres SNMP**

1.  Cree una instancia de la clase del sistema [**\_ \_ Namespace**](--namespace.md) mediante la compilación de un archivo [*.mof*](gloss-m.md) Managed Object Format o mediante la API COM para [WMI.](com-api-for-wmi.md)

    Para obtener más información, [vea Crear jerarquías dentro de WMI.](creating-hierarchies-within-wmi.md)

2.  Asocie calificadores [*de proveedor SNMP con*](gloss-q.md) la definición de espacio de nombres.

    Los calificadores de proveedor SNMP contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP accede a un dispositivo SNMP. Para obtener más información, vea [**Calificadores específicos del proveedor SNMP.**](qualifiers-specific-to-the-snmp-provider.md)

3.  Use la herramienta de línea de comandos [mofcomp](mofcomp.md) para cargar el código MOF en el repositorio WMI.

    Para obtener más información, [vea Compilación de archivos MOF.](compiling-mof-files.md)

En el ejemplo de código MOF siguiente se define el espacio de nombres snmp con un subconjunto de los calificadores que \\ se pueden asociar a un espacio de nombres SNMP.

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

## <a name="inserting-snmp-mib-data-into-wmi"></a>Inserción de datos MIB snmp en WMI

Como proveedor, el proveedor SNMP actúa como un puente entre los datos SNMP y las clases WMI. Por lo tanto, debe tener clases en WMI que representen distintos aspectos de un dispositivo habilitado para SNMP. Para ello, debe usar el compilador del módulo de información SNMP ([smi2smir](smi2smir.md)) para compilar información de administración de SNMP desde el formato SNMP en las definiciones de esquema CIM equivalentes. A continuación, puede dirigir la salida del compilador de información a una base de datos de esquema SNMP denominada "Repositorio de información del módulo SNMP (SMIR)" o a varios tipos diferentes de archivos MOF.

El compilador se ejecuta en el modo de línea de comandos, usando un archivo MIB como entrada. El comando siguiente carga el archivo MIB especificado en SMIRA.

**smi2smira /a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Configuración de comunidades SNMP

Como medida de seguridad, la comunidad "pública" de SNMP no se crea de forma predeterminada. Puede crear la comunidad como se describe en [Community Registry Configuración](/previous-versions/windows/embedded/ms907028(v=msdn.10)). Si no tiene ninguna comunidad, cree la comunidad "pública" para acceder al proveedor SNMP.

## <a name="generating-mof-files-from-mib-files"></a>Generar archivos MOF a partir de archivos MIB

Los siguientes comandos son un ejemplo de cómo generar archivos MOF a partir de los archivos MIB que se instalan cuando se instala el proveedor SNMP.

**cd** *%windir% \\ system32 \\ wbem \\ SNMP*

**Smi2smira /g ..** *\\ .. \\ hostmib.mib* **>** *hostmib.mof*

**Smi2smira /g ..** *\\ .. \\ ipforwd.mib* **>** *ipforwd.mof*

**Smi2smira /g ..** *\\ .. \\ nipx.mib* **>** *nipx.mof*

**Smi2smira /g ..** *\\ .. \\ mib \_ ii.mib* **>** *mib \_ ii.mof*

**Smi2smira /g ..** *\\ .. \\ lmmib2.mib* **>** *lmmib2.mof*

**Smi2smira /g ..** *\\ .. \\ mcastmib.mib* **>** *mcastmib.mof*

**Smi2smira /g ..** *\\ .. \\ rfc2571.mib* **>** *rfc2571.mof*

**Smi2smira /g ..** *\\ .. \\ wfospf.mib* **>** *wfospf.mof*

**Smi2smira /g ..** *\\ .. \\ dhcp.mib.. \\ .. \\ msft.mib* **>** *dhcp.mof*

**Smi2smira /g ..** *\\ .. \\ wins.mib.. \\ .. \\ msft.mib* **>** *wins.mof*

**Smi2smira /g ..** *\\ .. \\ mipx.mib.. \\ .. \\ msft.mib* **>** *mipx.mof*

**Smi2smira /g ..** *\\ .. \\ mripsap.mib.. \\ .. \\ msft.mib* **>** *mripsap.mof*

**Smi2smira /g ..** *\\ .. \\ msipbtp.mib.. \\ .. \\ msft.mib* **>** *msipbtp.mof*

**Smi2smira /g ..** *\\ .. \\ msiprip2.mib.. \\ .. \\ msft.mib* **>** *msiprip2.mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Adición de archivos MOF SNMP al repositorio WMI

Los comandos siguientes son un ejemplo de cómo agregar los archivos MOF que se generan a partir de los archivos MIB al repositorio WMI. Si desea agregar los archivos MOF a la lista de archivos que se restaurarán automáticamente en una recuperación del repositorio [*WMI,*](gloss-w.md) agregue la marca **-AUTORECOVER** al final de cada comando. Para obtener más información sobre la herramienta de línea Mofcomp.exe WMI, vea [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib.mof*

**mofcomp** *ipforwd.mof*

**mofcomp** *nipx.mof*

**mofcomp** *mib \_ ii.mof*

**mofcomp** *lmmib2.mof*

**mofcomp** *mcastmib.mof*

**mofcomp** *rfc2571.mof*

**mofcomp** *wfospf.mof*

**mofcomp** *dhcp.mof*

**mofcomp** *mipx.mof*

**mofcomp** *mripsap.mof*

**mofcomp** *msipbtp.mof*

**mofcomp** *msiprip2.mof*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 
