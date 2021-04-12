---
title: Consideraciones de 64 bits
description: Con la creciente disponibilidad de Windows de 64 bits, los usuarios esperan métodos de entrada, como teclados internacionales en varios idiomas o editores de métodos de entrada (IME) en idiomas de Asia oriental, para que funcionen correctamente con aplicaciones de 32 y 64 bits.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Text Services Framework (TSF), Windows de 64 bits
- TSF (marco de trabajo de servicios de texto), Windows de 64 bits
- servicios de texto, Windows de 64 bits
- Windows de 64 bits
- Text Services Framework (TSF), editor de métodos de entrada (IME)
- TSF (marco de trabajo de servicios de texto), editor de métodos de entrada (IME)
- servicios de texto, editor de métodos de entrada (IME)
- Editor de métodos de entrada (IME)
- IME (editor de métodos de entrada)
- Marco de trabajo de servicios de texto (TSF), teclados internacionales
- TSF (marco de trabajo de servicios de texto), teclados internacionales
- servicios de texto, teclados internacionales
- Teclados internacionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420879"
---
# <a name="64-bit-considerations"></a>Consideraciones de 64 bits

Con la creciente disponibilidad de Windows de 64 bits, los usuarios esperan métodos de entrada, como teclados internacionales en varios idiomas o editores de métodos de entrada (IME) en idiomas de Asia oriental, para que funcionen correctamente con aplicaciones de 32 y 64 bits. Al desarrollar componentes de métodos de entrada o servicios de texto para Microsoft Windows, es importante tener en cuenta Windows de 64 bits como una posible plataforma de destino para su producto.

Dado que los IME y los servicios de texto (basados en el marco de trabajo de servicios de texto) se implementan normalmente como bibliotecas de vínculos dinámicos (dll), es importante tener en cuenta que los archivos DLL se compilan específicamente para su uso en entornos de 32 bits o en entornos de 64 bits; las aplicaciones de 64 bits no pueden usar un archivo DLL creado para su uso en entornos de 32 bits y viceversa.

> [!Note]  
> WOW64 no mitiga esta restricción de DLL específica de bits. Para obtener información sobre WOW64, vea [ejecutar aplicaciones de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).

 

En este tema se describen las consideraciones de diseño importantes para desarrollar IME y servicios de texto para su uso en Windows de 64 bits.

## <a name="64-bit-considerations-for-imes"></a>64 consideraciones de bits para los IME

En esta sección se describen las consideraciones especiales relacionadas con la creación de IME para su uso con Windows de 64 bits. Para obtener información acerca de los IME, consulte [Editor de métodos de entrada](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Compilación de versiones de 32 bits y de 64 bits de un IME

Debido al problema de compatibilidad mencionado anteriormente de 32 bits y 64 bits con los archivos dll, se deben tomar algunas precauciones para asegurarse de que los IME funcionan de forma transparente con cualquier aplicación (32 bits o 64 bits) que se ejecute en Windows de 64 bits. La solución recomendada para permitir que el IME funcione de forma transparente con las aplicaciones de 32 bits y 64 bits en una plataforma de 64 bits es crear e instalar las versiones en paralelo de 32 bits y de 64 bits de la DLL de IME. Normalmente, los desarrolladores crean archivos dll paralelos desde un único origen mediante el ajuste de la configuración de la plataforma de destino en su entorno de compilación. Para obtener más información sobre las aplicaciones de un solo origen de 32 bits y de 64 bits, consulte [preparación para Windows de 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Instalación en paralelo de editores de métodos de entrada de 64 bits y 32 bits

Los desarrolladores de servicios de texto y IME deben tener en cuenta las consideraciones de 64 bits que se describen en este tema. Afortunadamente, los usuarios finales de estos servicios no deben preocuparse de estos detalles específicos de la implementación. Una característica de Windows de 64 bits es la posibilidad de ocultar las versiones de los archivos DLL del IME de 64 bits y de 32 de los usuarios finales. Cuando ambas versiones del IME están instaladas correctamente en paralelo, Windows de 64 bits reconoce la presencia de las versiones de 64 bits y de 32 bits del IME y presenta estos IME específicos de bits al usuario final como un solo IME *lógico* :. Cuando un usuario final necesita usar un IME, Windows de 64 bits elige de forma transparente la versión del IME (32 bits o 64 bits) que sea adecuada para las circunstancias determinadas.

En el caso de las instalaciones en paralelo de los IME de 64 y 32 bits para que funcionen correctamente (es decir, para representar los dos archivos dll específicos de la plataforma como un solo IME lógico para el usuario), deben cumplirse las siguientes condiciones:

-   Los desarrolladores deben crear versiones específicas de la plataforma (una para Windows de 32 bits y otra para Windows de 64 bits) de la DLL de IME.
-   Los archivos dll de 32 bits y 64 bits deben compartir el mismo nombre de archivo.
-   Deben seguirse los requisitos del directorio de instalación. Para obtener más información, consulte requisitos del directorio de instalación.

Las instalaciones en paralelo de los archivos dll de IME de 32 y 64 bits comparten la misma clave del registro para almacenar los datos de configuración (incluido el nombre de archivo DLL):


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



La función [**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) se usa para crear esta clave del registro. El programa de instalación y configuración de un IME debe llamar a esta función para registrar el IME como una distribución de teclado compatible. Solo se debe llamar a la función **ImmInstallIME** una vez, ya sea desde la versión de 32 bits o de 64 bits de la dll de IME.

## <a name="mismatched-ime-dlls"></a>Archivos dll de IME no coincidentes

No se recomienda ni se admite la instalación de la versión de 32 bits de un IME en Windows de 64 bits. Si una aplicación de 64 bits intenta cargar un IME de 32 bits, el IME produce un error en modo silencioso cuando la aplicación intenta cargar la distribución de teclado asociada.

> [!IMPORTANT]
>
> No se muestra ningún cuadro de diálogo o mensaje de advertencia cuando se produce un error de conflicto de aplicación de 64 bits o de 32 bits de IME.

 

64: consideraciones de bits para servicios de texto

En esta sección se describen las consideraciones especiales relacionadas con la creación de servicios de texto para su uso en entornos de 64 bits. Para obtener más información sobre los servicios de texto y el marco de trabajo de servicios de texto, vea [Text Services Framework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Compilación de servicios de texto de 32 y de 64 bits

Un servicio de texto se implementa como un objeto de modelo de objetos componentes (COM) expuesto en un archivo DLL. Por lo tanto, pueden producirse conflictos de DLL de 32 o 64 bits con los servicios de texto instalados en Windows de 64 bits. Al igual que con los IME, la solución recomendada para permitir que el servicio de texto funcione de forma transparente con las aplicaciones de 32 bits y 64 bits en una plataforma de 64 bits es crear e instalar las versiones en paralelo de 32 bits y de 64 bits de la DLL del servicio de texto.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Instalación en paralelo de los servicios de texto de 64 y 32 bits

Para una versión de 32 bits y una versión de 64 bits de un servicio de texto que se instalará en paralelo y se representará al usuario como un servicio de texto lógico único, deben cumplirse las siguientes condiciones:

-   Ambas versiones del servicio de texto especifican el mismo identificador de clase (CLSID) cuando se registran con el subsistema COM.
-   Ambas versiones del servicio de texto se registran de forma independiente. Para obtener más información, vea [registrar aplicaciones com](/windows/desktop/com/registering-com-applications).

Cuando un servicio de texto de 32 bits se registra con Windows de 64 bits, la operación de registro se redirige de forma transparente a la siguiente clave del registro:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Redirector del registro](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[Registro del servicio de texto](text-service-registration.md) de ITfInputProcessorProfiles

La versión de 64 bits y la versión de 32 bits de un servicio de texto pueden estar en uso al mismo tiempo. En los casos en que ambas versiones de un servicio de texto necesitan manipular los objetos compartidos, la coordinación para el acceso a los objetos compartidos debe estar diseñada en el servicio de texto. Cada servicio de texto es responsable de administrar los objetos compartidos que se usan o son necesarios.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Instalación de solo servicios de texto de 32 bits en Windows de 64 bits

No se recomienda ni se admite la instalación de la versión de 32 bits de un servicio de texto en una plataforma de Windows de 64 bits. Debido a la asignación de registro que se realiza en las plataformas de Windows de 64 bits, una aplicación de 64 bits puede enumerar los servicios de un servicio de texto de 32 bits a través de la interfaz **ITfInputProcessorProfiles** . Sin embargo, si una aplicación de 64 bits intenta cargar un servicio de texto de 32 bits, se produce un error en la carga de forma silenciosa.

> [!IMPORTANT]
>
> No se muestra ningún cuadro de diálogo o mensaje de advertencia cuando se produce un error de conflicto de aplicación de 64 bits/servicio de texto de 32 bits.

 

Otras consideraciones

## <a name="installation-directory-requirements"></a>Requisitos del directorio de instalación

En esta sección se describen los requisitos para instalar los archivos binarios de IME y de servicio de texto. Si no se siguen estos requisitos, es posible que el servicio de texto o el IME no funcionen correctamente.

**DLLs IME**

En las plataformas de Windows de 64 bits, instale las dll de IME de 32 bits y de 64 bits en los directorios siguientes:

-   Instale las dll de IME de 32 bits en el directorio del sistema SysWOW64; Llame a [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)o a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con **CSIDL \_ SYSTEMX86** para recuperar esta ruta de acceso al directorio. Como alternativa, si usa [Windows Installer](/windows/desktop/Msi/about-windows-installer), use la propiedad [**carpetadelsistema**](/windows/desktop/Msi/systemfolder) .
-   Instale las dll de IME de 64 bits en el directorio del sistema system32; Llame a [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)o a **SHGetFolderPath** con el [ \_ sistema CSIDL](/windows/desktop/shell/csidl) para recuperar esta ruta de acceso al directorio. O bien, para Windows Installer, use la propiedad [**System64Folder**](/windows/desktop/Msi/system64folder) .

**Archivos dll de servicio de texto y archivos binarios relacionados**

En las plataformas de Windows de 64 bits, instale las dll de servicio de texto de 32 bits y de 64 bits, así como cualquier otro archivo binario relacionado con el servicio de texto o con el IME, en los directorios siguientes:

-   Instale los archivos dll de servicio de texto de 32 bits y cualquier otro archivo binario de 32 bits en un subdirectorio en el directorio de archivos de programa (x86). Llame a **SHGetFolderPath** con el programa de la **\_ \_ FILESX86** para recuperar esta ruta de acceso al directorio. O bien, para Windows Installer, use la propiedad [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) .
-   Instale los archivos dll de servicio de texto de 64 bits y cualquier otro archivo binario de 64 bits en un subdirectorio del directorio archivos de programa; Llame a **SHGetFolderPath** con **\_ \_ los archivos de programa CSIDL** para recuperar esta ruta de acceso al directorio. O bien, para Windows Installer, use la propiedad [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) .

Si no usa un paquete de Windows Installer para instalar el IME o el servicio de texto, es muy recomendado que use una aplicación de instalación de 64 bits. El redirector del sistema de archivos WOW64 podría hacer que los instaladores de 32 bits colocaran archivos en directorios incorrectos (por ejemplo, la redirección del sistema de archivos WOW64 podría provocar que los archivos destinados al directorio system32 se instalen en el directorio SysWOW64 en su lugar). Si debe usar un instalador de 32 bits, deshabilite la redirección de archivos WOW64 durante el proceso de instalación para asegurarse de que el servicio de redireccionamiento de archivos no provoca ninguna redirección imprevista durante el proceso de instalación. Para obtener información sobre el redirector del sistema de archivos WOW64, consulte [redirector del sistema de archivos](/windows/desktop/WinProg64/file-system-redirector). Para obtener información sobre cómo deshabilitar o habilitar la redirección del sistema de archivos WOW64, vea [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Evite las rutas de instalación codificadas de forma rígida. Para obtener más información, vea [Buscar directorios mediante la interfaz de programación de aplicaciones no Hard-Coded rutas de](/previous-versions//ms675638(v=vs.85)) acceso

 

> [!IMPORTANT]
>
> No instale ningún archivo de IME o de servicio de texto en el directorio especial% WINDIR% \\ IME (de forma predeterminada, c: \\ Windows \\ IME). Este directorio contiene archivos del sistema que admiten servicios de texto y IME; no está diseñado para contener ningún archivo de IME o de servicio de texto de terceros y no se admite el redireccionamiento del sistema de archivos WOW64 para este directorio.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Dos procesos de Ctfmon.exe se ejecutan en plataformas de Windows de 64 bits

El proceso de ctfmon.exe administra el marco de trabajo de servicios de texto en el escritorio y también proporciona la interfaz de usuario (UI) de la barra de idioma. En Windows de 64 bits, una versión de 32 bits y una versión de 64 bits del proceso de ctfmon.exe se ejecutan simultáneamente. El proceso de ctfmon.exe de bits de 64 administra los servicios de texto de 64 bits y, del mismo modo, el proceso de ctfmon.exe de 32 bits administra los servicios de texto de 32 bits.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Comportamiento de presentación para diferentes versiones de la interfaz de usuario de la barra de idioma

En Windows de 64 bits, siempre se muestra la interfaz de usuario de la barra de idioma asociada a la versión de 64 bits de un servicio de texto. En los casos en los que una aplicación de 32 bits usa la versión de 32 bits de un servicio de texto, Windows de 64 bits inserta automáticamente la interfaz de usuario de la barra de idioma para el servicio de texto de 64 bits equivalente. Esto garantiza que no se requiere ningún trabajo especial para que los servicios de texto de 32 bits aparezcan en la versión de 64 bits de la barra de idioma.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Consideraciones del panel de control en Windows de 64 bits

Windows de 64 bits proporciona acceso a las versiones de los servicios de texto y los IME de 32 bits y 64 a través del panel de control. Para obtener acceso a la configuración del panel de control para versiones específicas de los servicios de texto o IME, busque en las siguientes ubicaciones.

-   **Acceso al panel de control para los servicios de texto y IME de 32 bits:** Configuración de inicio >-> panel de control-> Ver iconos del panel de control x86
-   **Acceso al panel de control para los servicios de texto y IME de 64 bits:** Configuración de inicio >-> panel de control-> opciones de configuración regional y de idioma

Puede haber casos en los que algunas opciones de configuración solo estén disponibles a través del panel de control de 32 bits. En estos casos, asegúrese de que los usuarios del servicio de texto o el IME son conscientes de esto, proporcionando la documentación adecuada o ofreciendo sugerencias de interfaz de usuario en la interfaz de configuración de 64 bits.

 

 