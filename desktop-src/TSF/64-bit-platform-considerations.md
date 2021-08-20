---
title: Consideraciones de 64 bits
description: Con la disponibilidad creciente de los Windows de 64 bits, los usuarios esperan que los métodos de entrada, como teclados internacionales en varios idiomas o editores de métodos de entrada (IME) en idiomas de Asia Oriental, funcionen correctamente con aplicaciones de 32 y 64 bits.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Text Services Framework (TSF), 64 bits Windows
- TSF (Text Services Framework),64 bits Windows
- servicios de texto,64 bits Windows
- Windows de 64 bits
- Text Services Framework (TSF),Editor de métodos de entrada (IME)
- TSF (Text Services Framework),Editor de métodos de entrada (IME)
- text services,Input Method Editor (IME)
- Editor de métodos de entrada (IME)
- IME (Editor de métodos de entrada)
- Text Services Framework (TSF), teclados internacionales
- TSF (Text Services Framework), teclados internacionales
- servicios de texto, teclados internacionales
- teclados internacionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de076721f1be036f0e5db6ea74b52a50060b9f0742621188a799ef6c824f677a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880101"
---
# <a name="64-bit-considerations"></a>Consideraciones de 64 bits

Con la disponibilidad creciente de los Windows de 64 bits, los usuarios esperan que los métodos de entrada, como teclados internacionales en varios idiomas o editores de métodos de entrada (IME) en idiomas de Asia Oriental, funcionen correctamente con aplicaciones de 32 y 64 bits. Al desarrollar componentes de métodos de entrada o servicios de texto para Microsoft Windows, es importante considerar los Windows de 64 bits como una plataforma de destino potencial para su producto.

Dado que los EME y los servicios de texto (basados en Text Services Framework) se implementan normalmente como bibliotecas de vínculos dinámicos (DLL), es importante tener en cuenta que los archivos DLL se han creado específicamente para su uso en entornos de 32 bits o entornos de 64 bits. Las aplicaciones de 64 bits no pueden usar un archivo DLL creado para su uso en entornos de 32 bits, y viceversa.

> [!Note]  
> WOW64 no mitiga esta restricción dll específica del bit. Para obtener información sobre WOW64, vea [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).

 

En este tema se de abordan consideraciones de diseño importantes para el desarrollo de imes y servicios de texto para su uso en archivos de 64 Windows.

## <a name="64-bit-considerations-for-imes"></a>Consideraciones de 64 bits para los IME

En esta sección se describen las consideraciones especiales implicadas en la creación de IME para su uso con archivos de 64 Windows. Para obtener información sobre los IME, vea [Editor de métodos de entrada](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Creación de versiones de 32 y 64 bits de un IME

Debido al problema de compatibilidad de 32 bits o 64 bits mencionado anteriormente con los archivos DLL, se deben tomar algunas precauciones para asegurarse de que los IME funcionan de forma transparente con cualquier aplicación (de 32 o 64 bits) que se ejecute en archivos de 64 Windows. La solución recomendada para permitir que el IME funcione de forma transparente con aplicaciones de 32 y 64 bits en una plataforma de 64 bits es compilar e instalar versiones paralelas de 32 y 64 bits del archivo DLL de IME. Normalmente, los desarrolladores crean archivos DLL paralelos desde un único origen ajustando la configuración de la plataforma de destino en su entorno de compilación. Para obtener más información sobre las aplicaciones de 32 y 64 bits de un solo aprovisionamiento, vea [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Instalación en paralelo de editores de métodos de entrada de 64 y 32 bits

Los desarrolladores de IME y servicios de texto deben tener en cuenta las consideraciones de 64 bits que se describen en este tema. Afortunadamente, los usuarios finales de estos servicios no necesitan preocuparse por estos detalles específicos de la implementación. Una característica de los archivos DLL de 64 Windows es la capacidad de ocultar a los usuarios finales la necesidad de versiones específicas de 64 y 32 bits de los archivos DLL de IME. Cuando ambas versiones del IME se instalan correctamente en paralelo, Windows de 64 bits reconoce la presencia de las versiones de 64 y 32 bits del IME y presenta estos IME específicos del bit al usuario final como un *único* IME lógico. Cuando un usuario final necesita usar un IME, Windows de 64 bits elige de forma transparente la versión del IME (32 o 64 bits) que sea adecuada para las circunstancias dadas.

Para que las instalaciones en paralelo de EME de 64 y 32 bits funcionen correctamente (es decir, para representar los dos archivos DLL específicos de la plataforma como un único IME lógico para el usuario), se deben cumplir las condiciones siguientes:

-   Los desarrolladores deben compilar versiones específicas de la plataforma (una para archivos de Windows de 32 bits y otra para archivos Windows de 64 bits) del archivo DLL de IME.
-   Los archivos DLL de 32 y 64 bits deben compartir el mismo nombre de archivo.
-   Se deben seguir los requisitos del directorio de instalación. Para obtener más información, vea Requisitos del directorio de instalación.

Las instalaciones en paralelo de archivos DLL de IME de 32 y 64 bits comparten la misma clave del Registro para almacenar los datos de configuración (incluido el nombre del archivo DLL):


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



La [**función ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) se usa para crear esta clave del Registro. El programa de instalación e instalación de un IME debe llamar a esta función para registrar el IME como un diseño de teclado compatible. Se debe llamar a la función **ImmInstallIME** solo una vez, ya sea desde la versión de 32 o 64 bits del archivo DLL de IME.

## <a name="mismatched-ime-dlls"></a>Archivos DLL de IME no coincidentes

No se recomienda ni se admite la instalación solo de la versión de 32 bits de un IME en Windows de 64 bits. Si una aplicación de 64 bits intenta cargar un IME de 32 bits, el IME produce un error en modo silencioso cuando la aplicación intenta cargar el diseño de teclado asociado.

> [!IMPORTANT]
>
> No se muestra ningún mensaje o cuadro de diálogo de advertencia cuando se produce un error de conflicto de IME de aplicación de 64 bits o IME de 32 bits.

 

Consideraciones de 64 bits para Text Services

En esta sección se describen las consideraciones especiales implicadas en la creación de servicios de texto para su uso en entornos de 64 bits. Para obtener más información sobre los servicios de texto y Text Services Framework, [vea Text Services Framework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Creación de servicios de texto de 32 y 64 bits

Un servicio de texto se implementa como un objeto del Modelo de objetos componentes (COM) expuesto en un archivo DLL. Por lo tanto, pueden producirse conflictos de DLL de 32 o 64 bits con servicios de texto instalados en archivos de 64 Windows. Al igual que con los IME, la solución recomendada para permitir que el servicio de texto funcione de forma transparente con aplicaciones de 32 y 64 bits en una plataforma de 64 bits es compilar e instalar versiones paralelas de 32 y 64 bits del archivo DLL del servicio de texto.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Instalación en paralelo de servicios de texto de 64 y 32 bits

Para que una versión de 32 bits y una versión de 64 bits de un servicio de texto se instalen en paralelo y se represente al usuario como un único servicio de texto lógico, deben cumplirse las condiciones siguientes:

-   Ambas versiones del servicio de texto especifican el mismo identificador de clase (CLSID) cuando se registran con el subsistema COM.
-   Ambas versiones del servicio de texto se registran de forma independiente. Para obtener más información, [vea Registrar aplicaciones COM.](/windows/desktop/com/registering-com-applications)

Cuando se registra un servicio de texto de 32 bits con una Windows de 64 bits, la operación de registro se redirige de forma transparente a la siguiente clave del Registro:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Redirector del Registro](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



Registro del servicio de texto [ITfInputProcessorProfiles](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[](text-service-registration.md)

La versión de 64 bits y la versión de 32 bits de un servicio de texto podrían estar en uso simultáneamente. En los casos en los que ambas versiones de un servicio de texto necesitan manipular objetos compartidos, la coordinación para el acceso a los objetos compartidos debe diseñarse en el servicio de texto. Cada servicio de texto es responsable de administrar los objetos compartidos que se usan o se necesitan.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Instalar solo servicios de texto de 32 bits en servicios de 64 Windows

No se recomienda ni se admite la instalación solo de la versión de 32 bits de un servicio de texto en una plataforma de Windows de 64 bits. Debido a la asignación de registro que se realiza en plataformas de Windows de 64 bits, una aplicación de 64 bits puede enumerar los servicios de un servicio de texto de 32 bits a través de la interfaz **ITfInputProcessorProfiles.** Sin embargo, si una aplicación de 64 bits intenta cargar un servicio de texto de 32 bits, se produce un error en la carga en modo silencioso.

> [!IMPORTANT]
>
> No se muestra ningún mensaje o cuadro de diálogo de advertencia cuando se produce un error de conflicto de servicio de texto de aplicación de 64 bits o de 32 bits.

 

Otras consideraciones

## <a name="installation-directory-requirements"></a>Requisitos del directorio de instalación

En esta sección se describen los requisitos para dónde instalar los archivos binarios del servicio de texto y IME. Si no se siguen estos requisitos, es posible que el servicio de texto o el IME no funcionen correctamente.

**Archivos DLL de IME**

En las plataformas Windows de 64 bits, instale los archivos DLL de IME de 32 y 64 bits en los directorios siguientes:

-   Instale archivos DLL de IME de 32 bits en el directorio del sistema SysWOW64; llame [**a GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con **CSIDL \_ SYSTEMX86** para recuperar esta ruta de acceso del directorio. Como alternativa, si usa el instalador [Windows](/windows/desktop/Msi/about-windows-installer), use la [**propiedad SystemFolder.**](/windows/desktop/Msi/systemfolder)
-   Instale archivos DLL de IME de 64 bits en el directorio del sistema System32; llame [**a GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)o **SHGetFolderPath** con [CSIDL \_ SYSTEM](/windows/desktop/shell/csidl) para recuperar esta ruta de acceso del directorio. O bien, para Windows instalador, use la [**propiedad System64Folder.**](/windows/desktop/Msi/system64folder)

**Archivos DLL del servicio de texto y archivos binarios relacionados**

En las plataformas Windows de 64 bits, instale los archivos DLL del servicio de texto de 32 y 64 bits, así como cualquier otro archivo binario relacionado con el servicio de texto o el IME, en los directorios siguientes:

-   Instale archivos DLL del servicio de texto de 32 bits y cualquier otro archivo binario de 32 bits en un subdirectorio del directorio Archivos de programa (x86); llame **a SHGetFolderPath** con **CSIDL \_ PROGRAM \_ FILESX86** para recuperar esta ruta de acceso del directorio. O bien, para Windows instalador, use la [**propiedad ProgramFilesFolder.**](/windows/desktop/Msi/programfilesfolder)
-   Instale archivos DLL del servicio de texto de 64 bits y cualquier otro archivo binario de 64 bits en un subdirectorio en el directorio Archivos de programa. llame **a SHGetFolderPath** con **ARCHIVOS DE PROGRAMA CSIDL \_ para \_** recuperar esta ruta de acceso del directorio. O bien, para Windows instalador, use la [**propiedad ProgramFiles64Folder.**](/windows/desktop/Msi/programfiles64folder)

Si no usa un paquete de Windows Installer para instalar el IME o el servicio de texto, se recomienda encarecidamente que use una aplicación de instalación de 64 bits. El redirector del sistema de archivos WOW64 podría hacer que los instaladores de 32 bits coloquen archivos en directorios incorrectos (por ejemplo, el redireccionamiento del sistema de archivos WOW64 podría hacer que los archivos destinados al directorio System32 se instalaran en el directorio SysWOW64 en su lugar). Si debe usar un instalador de 32 bits, deshabilite el redireccionamiento de archivos WOW64 durante el proceso de instalación para asegurarse de que el servicio de redirección de archivos no provoca ningún redireccionamiento no deseado durante el proceso de instalación. Para obtener información sobre el redirector del sistema de archivos WOW64, vea [Redireccionamiento del sistema de archivos](/windows/desktop/WinProg64/file-system-redirector). Para obtener información sobre cómo deshabilitar o habilitar el redireccionamiento del sistema de archivos WOW64, vea [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Evite las rutas de instalación codificadas de forma automática. Para obtener más información, vea [Buscar directorios mediante la interfaz de programación](/previous-versions//ms675638(v=vs.85)) de aplicaciones no Hard-Coded rutas de acceso

 

> [!IMPORTANT]
>
> No instale ningún archivo de servicio de texto o IME en el directorio especial %WINDIR% \\ IME (de forma predeterminada, c: \\ Windows \\ IME ). Este directorio contiene archivos del sistema que admiten servicios de texto e IME; no está diseñado para contener archivos de servicio de texto o IME de terceros, y no se admite el redireccionamiento del sistema de archivos WOW64 para este directorio.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Los procesos Ctfmon.exe duales se ejecutan en plataformas de Windows de 64 bits

El ctfmon.exe de usuario administra el Text Services Framework en el escritorio y también proporciona la interfaz de usuario (UI) de la barra de idioma. En el proceso de Windows 64 bits, se ejecutan simultáneamente una versión de 32 bits y una versión de 64 bits del ctfmon.exe de 64 bits. El proceso de ctfmon.exe de 64 bits administra servicios de texto de 64 bits y, del mismo modo, el proceso de ctfmon.exe de 32 bits administra los servicios de texto de 32 bits.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Mostrar el comportamiento de las distintas versiones de la interfaz de usuario de la barra de lenguaje

En las versiones de 64 Windows, solo se muestra la interfaz de usuario de la barra de idioma asociada a la versión de 64 bits de un servicio de texto. En los casos en los que una aplicación de 32 bits usa la versión de 32 bits de un servicio de texto, Windows de 64 bits inserta automáticamente la interfaz de usuario de la barra de idioma para el servicio de texto de 64 bits equivalente. Esto garantiza que no se requiere ningún trabajo especial para que los servicios de texto de 32 bits aparezcan en la versión de 64 bits de la barra de idioma.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Panel de control consideraciones sobre los datos de 64 bits Windows

El Windows de 64 bits proporciona acceso a las versiones de 32 y 64 bits de los servicios de texto y de los EME a través del Panel de control. Para acceder a Panel de control configuración de versiones específicas de servicios de texto o IME, busque en las siguientes ubicaciones.

-   Panel de control acceso para Servicios de texto e IME de **32 bits:** Iniciar -> Configuración -> Panel de control -> iconos de Panel de control x86
-   Panel de control acceso para Servicios de texto e IME de **64 bits:** Start -> Configuración -> Panel de control -> Regional and Language Options

Puede haber circunstancias en las que algunas configuraciones solo estén disponibles a través de la configuración de 32 Panel de control. En estos casos, asegúrese de que los usuarios de su servicio de texto o IME son conscientes de esto, proporcionando la documentación adecuada u ofreciendo sugerencias de interfaz de usuario en la interfaz de configuración de 64 bits.

 

 