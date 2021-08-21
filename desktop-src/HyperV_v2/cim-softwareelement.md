---
description: Representa una parte que se puede administrar individualmente o que se puede implementar de un \_ objeto SoftwareFeature de CIM.
ms.assetid: 96affc55-b001-4122-b883-3610bf95a786
title: CIM_SoftwareElement (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.Version
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.LanguageEdition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6454b6080a4841ef261233ce304725ec4a08a1a793cfb657c87e20ef56592df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647365"
---
# <a name="cim_softwareelement-class-hyper-v-management"></a>CIM_SoftwareElement (administración de Hyper-V)

Representa una parte que se puede administrar individualmente o que se puede implementar de un **\_ objeto SoftwareFeature de CIM.**

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Application::DeploymentModel"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string Name;
  string Version;
  uint16 SoftwareElementState;
  string SoftwareElementID;
  uint16 TargetOperatingSystem;
  string OtherTargetOS;
  string Manufacturer;
  string BuildNumber;
  string SerialNumber;
  string CodeSet;
  string IdentificationCode;
  string LanguageEdition;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim SoftwareElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM SoftwareElement** tiene estas propiedades.

<dl> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.4")
</dt> </dl>

Identificador interno de la compilación del elemento de software.

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Codificación de caracteres utilizada por el elemento de software, como UTF-8 e ISO8859-1.

</dd> <dt>

**Código de identificación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001.6")
</dt> </dl>

Identificador del fabricante del elemento de software. Suele ser una unidad de almacén (SKU) o un número de pieza.

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001.7")
</dt> </dl>

Edición de idioma del elemento de software. Se deben usar los códigos de idioma definidos en el estándar ISO 639. Si el elemento representa una versión multilingüe o internacional, se debe usar la cadena "Multilingüe".

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001.3")
</dt> </dl>

Fabricante del elemento de software.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre utilizado para identificar el elemento de software.

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")
</dt> </dl>

El fabricante y el tipo de sistema operativo cuando la **propiedad TargetOperatingSystem** se establece en **Other** ("1").

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.4")
</dt> </dl>

Número de serie asignado del elemento de software.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador del elemento de software que se usará junto con otras claves para crear una identificación única del elemento.

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Estado del ciclo de vida del elemento de software.

\- Un SoftwareElement en estado implementable describe los detalles necesarios para distribuirlo correctamente y los detalles (comprobaciones y acciones) necesarios para moverlo al estado instalable (es decir, el siguiente estado).

\- Un SoftwareElement en estado instalable describe los detalles necesarios para instalarlo correctamente y los detalles (comprobaciones y acciones) necesarios para crear un elemento en el estado ejecutable (es decir, el siguiente estado).

\- Un SoftwareElement en estado ejecutable describe los detalles necesarios para iniciarlo correctamente y los detalles (Comprobaciones y acciones) necesarios para moverlo al estado en ejecución (es decir, el siguiente estado).

\- Un SoftwareElement en estado de ejecución describe los detalles necesarios para administrar el elemento iniciado.

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

**Implementable** (0)


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

**Instalable** (1)


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

**Ejecutable** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**En** ejecución (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")
</dt> </dl>

Sistema operativo del elemento de software. El valor de esta propiedad no garantiza que sea ejecutable binario.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

**MACOS** (2)


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Tru64_UNIX"></span><span id="tru64_unix"></span><span id="TRU64_UNIX"></span>

**Tru64 UNIX** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

**SISTEMA OPERATIVO/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

**WINCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

**Sequent** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

**IIONES** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

**Solaris** (29)


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OS"></span><span id="hp_nonstop_os"></span><span id="HP_NONSTOP_OS"></span>

**SISTEMA OPERATIVO HP nonStop** (33)


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OSS"></span><span id="hp_nonstop_oss"></span><span id="HP_NONSTOP_OSS"></span>

**HP NonStop OSS** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

**Estorba** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM"></span><span id="vm"></span>

**VM** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

**Kernel de MACH** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

**NextStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**Dedicado** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

**OS/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

**TPF** (62)


</dt> <dd></dd> <dt>

<span id="Windows__R__Me"></span><span id="windows__r__me"></span><span id="WINDOWS__R__ME"></span>

**Windows (R) Me** (63)


</dt> <dd></dd> <dt>

<span id="Caldera_Open_UNIX"></span><span id="caldera_open_unix"></span><span id="CALDERA_OPEN_UNIX"></span>

**Puerta Open UNIX** (64)


</dt> <dd></dd> <dt>

<span id="OpenBSD"></span><span id="openbsd"></span><span id="OPENBSD"></span>

**OpenBSD** (65)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (66)


</dt> <dd></dd> <dt>

<span id="Windows_XP"></span><span id="windows_xp"></span><span id="WINDOWS_XP"></span>

**Windows XP** (67)


</dt> <dd></dd> <dt>

<span id="z_OS"></span><span id="z_os"></span><span id="Z_OS"></span>

**z/OS** (68)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003"></span><span id="microsoft_windows_server_2003"></span><span id="MICROSOFT_WINDOWS_SERVER_2003"></span>

**Microsoft Windows Server 2003** (69)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003_64-Bit"></span><span id="microsoft_windows_server_2003_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2003_64-BIT"></span>

**Microsoft Windows Server 2003 de 64 bits** (70)


</dt> <dd></dd> <dt>

<span id="Windows_XP_64-Bit"></span><span id="windows_xp_64-bit"></span><span id="WINDOWS_XP_64-BIT"></span>

**Windows XP de 64 bits** (71)


</dt> <dd></dd> <dt>

<span id="Windows_XP_Embedded"></span><span id="windows_xp_embedded"></span><span id="WINDOWS_XP_EMBEDDED"></span>

**Windows XP Embedded** (72)


</dt> <dd></dd> <dt>

<span id="Windows_Vista"></span><span id="windows_vista"></span><span id="WINDOWS_VISTA"></span>

**Windows Vista** (73)


</dt> <dd></dd> <dt>

<span id="Windows_Vista_64-Bit"></span><span id="windows_vista_64-bit"></span><span id="WINDOWS_VISTA_64-BIT"></span>

**Windows Vista de 64 bits** (74)


</dt> <dd></dd> <dt>

<span id="Windows_Embedded_for_Point_of_Service"></span><span id="windows_embedded_for_point_of_service"></span><span id="WINDOWS_EMBEDDED_FOR_POINT_OF_SERVICE"></span>

**Windows embedded for Point of Service** (75)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008"></span><span id="microsoft_windows_server_2008"></span><span id="MICROSOFT_WINDOWS_SERVER_2008"></span>

**Microsoft Windows Server 2008** (76)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_64-Bit"></span><span id="microsoft_windows_server_2008_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_64-BIT"></span>

**Microsoft Windows Server 2008 de 64 bits** (77)


</dt> <dd></dd> <dt>

<span id="FreeBSD_64-Bit"></span><span id="freebsd_64-bit"></span><span id="FREEBSD_64-BIT"></span>

**FreeBSD de 64 bits** (78)


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux"></span><span id="redhat_enterprise_linux"></span><span id="REDHAT_ENTERPRISE_LINUX"></span>

**RedHat Enterprise Linux** (79)


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux_64-Bit"></span><span id="redhat_enterprise_linux_64-bit"></span><span id="REDHAT_ENTERPRISE_LINUX_64-BIT"></span>

**RedHat Enterprise Linux de 64 bits** (80)


</dt> <dd></dd> <dt>

<span id="Solaris_64-Bit"></span><span id="solaris_64-bit"></span><span id="SOLARIS_64-BIT"></span>

**Solaris de 64 bits** (81)


</dt> <dd></dd> <dt>

<span id="SUSE"></span><span id="suse"></span>

**SUSE** (82)


</dt> <dd></dd> <dt>

<span id="SUSE_64-Bit"></span><span id="suse_64-bit"></span><span id="SUSE_64-BIT"></span>

**SUSE de 64 bits** (83)


</dt> <dd></dd> <dt>

<span id="SLES"></span><span id="sles"></span>

**SLES** (84)


</dt> <dd></dd> <dt>

<span id="SLES_64-Bit"></span><span id="sles_64-bit"></span><span id="SLES_64-BIT"></span>

**SLES de 64 bits** (85)


</dt> <dd></dd> <dt>

<span id="Novell_OES"></span><span id="novell_oes"></span><span id="NOVELL_OES"></span>

**OES Desasoy** (86)


</dt> <dd></dd> <dt>

<span id="Novell_Linux_Desktop"></span><span id="novell_linux_desktop"></span><span id="NOVELL_LINUX_DESKTOP"></span>

**Escritorio De Linux de Linux** de Linux (87)


</dt> <dd></dd> <dt>

<span id="Sun_Java_Desktop_System"></span><span id="sun_java_desktop_system"></span><span id="SUN_JAVA_DESKTOP_SYSTEM"></span>

**Sun Java Desktop System** (88)


</dt> <dd></dd> <dt>

<span id="Mandriva"></span><span id="mandriva"></span><span id="MANDRIVA"></span>

**Mandriva** (89)


</dt> <dd></dd> <dt>

<span id="Mandriva_64-Bit"></span><span id="mandriva_64-bit"></span><span id="MANDRIVA_64-BIT"></span>

**Mandriva de 64 bits** (90)


</dt> <dd></dd> <dt>

<span id="TurboLinux"></span><span id="turbolinux"></span><span id="TURBOLINUX"></span>

**TurboLinux** (91)


</dt> <dd></dd> <dt>

<span id="TurboLinux_64-Bit"></span><span id="turbolinux_64-bit"></span><span id="TURBOLINUX_64-BIT"></span>

**TurboLinux de 64 bits** (92)


</dt> <dd></dd> <dt>

<span id="Ubuntu"></span><span id="ubuntu"></span><span id="UBUNTU"></span>

**Ubuntu** (93)


</dt> <dd></dd> <dt>

<span id="Ubuntu_64-Bit"></span><span id="ubuntu_64-bit"></span><span id="UBUNTU_64-BIT"></span>

**Ubuntu de 64 bits** (94)


</dt> <dd></dd> <dt>

<span id="Debian"></span><span id="debian"></span><span id="DEBIAN"></span>

**Debian** (95)


</dt> <dd></dd> <dt>

<span id="Debian_64-Bit"></span><span id="debian_64-bit"></span><span id="DEBIAN_64-BIT"></span>

**Debian de 64 bits** (96)


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x"></span><span id="linux_2.4.x"></span><span id="LINUX_2.4.X"></span>

**Linux 2.4.x** (97)


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x_64-Bit"></span><span id="linux_2.4.x_64-bit"></span><span id="LINUX_2.4.X_64-BIT"></span>

**Linux 2.4.x de 64 bits** (98)


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x"></span><span id="linux_2.6.x"></span><span id="LINUX_2.6.X"></span>

**Linux 2.6.x** (99)


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x_64-Bit"></span><span id="linux_2.6.x_64-bit"></span><span id="LINUX_2.6.X_64-BIT"></span>

**Linux 2.6.x de 64 bits** (100)


</dt> <dd></dd> <dt>

<span id="Linux_64-Bit"></span><span id="linux_64-bit"></span><span id="LINUX_64-BIT"></span>

**Linux de 64 bits** (101)


</dt> <dd></dd> <dt>

<span id="Other_64-Bit"></span><span id="other_64-bit"></span><span id="OTHER_64-BIT"></span>

**Otros 64 bits** (102)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_R2"></span><span id="microsoft_windows_server_2008_r2"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_R2"></span>

**Microsoft Windows Server 2008 R2** (103)


</dt> <dd></dd> <dt>

<span id="VMware_ESXi"></span><span id="vmware_esxi"></span><span id="VMWARE_ESXI"></span>

**VMware ESXi** (104)


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_7"></span><span id="microsoft_windows_7"></span><span id="MICROSOFT_WINDOWS_7"></span>

**Microsoft Windows 7** (105)


</dt> <dd></dd> <dt>

<span id="CentOS_32-bit"></span><span id="centos_32-bit"></span><span id="CENTOS_32-BIT"></span>

**CentOS de 32 bits** (106)


</dt> <dd></dd> <dt>

<span id="CentOS_64-bit"></span><span id="centos_64-bit"></span><span id="CENTOS_64-BIT"></span>

**CentOS de 64 bits** (107)


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_32-bit"></span><span id="oracle_enterprise_linux_32-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_32-BIT"></span>

**Oracle Enterprise Linux de 32 bits** (108)


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_64-bit"></span><span id="oracle_enterprise_linux_64-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_64-BIT"></span>

**Oracle Enterprise Linux de 64 bits** (109)


</dt> <dd></dd> <dt>

<span id="eComStation_32-bitx"></span><span id="ecomstation_32-bitx"></span><span id="ECOMSTATION_32-BITX"></span>

**eComStation 32 bitsx** (110)


</dt> <dd></dd> </dl>

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001.4")
</dt> </dl>

La versión de software con el formato *<Major>* *<Minor>* .*<Revision>* o *<Major>* *<Minor><letter><revision>* .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> </dl>

 

