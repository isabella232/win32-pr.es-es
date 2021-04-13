---
title: Instalar y registrar controladores de protocolo (características heredadas del entorno de Windows)
description: La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y registrarlos.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359651"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Instalar y registrar controladores de protocolo (características heredadas del entorno de Windows)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

La instalación de **controladores de protocolo** implica copiar los archivos dll en una ubicación adecuada en el directorio de archivos de programa y registrarlos.

Esta sección contiene los siguientes temas:

-   [Instrucciones de instalación](#installation-guidelines)
-   [Para registrar los controladores de protocolo](#to-register-protocol-handlers)
-   [Para registrar extensiones de Shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Instrucciones de instalación

Los controladores de protocolo deben implementar el registro automático para la instalación y deben seguir estas directrices:

-   El instalador debe utilizar el instalador EXE o MSI.
-   Se deben proporcionar las notas de la versión.
-   Se debe crear una entrada **Agregar o quitar programas** para cada complemento instalado.
-   El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.
-   Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo de nuevo en el complemento predeterminado para ese tipo de archivo.

## <a name="to-register-protocol-handlers"></a>Para registrar los controladores de protocolo

Debe hacer 14 entradas en el registro para registrar el componente de controlador de protocolo, donde:

-   *Ver \_ Ind \_ ProgID* es el ProgID independiente de la versión de la implementación del controlador de protocolo.
-   *Ver \_ \_Identificador de programa (ProgID* ) de DEP es el ProgID dependiente de la versión de la implementación del controlador de protocolo
-   *CLSID \_ 1* es el CLSID de la implementación del controlador de protocolo

1.  Registre el ProgID independiente de la versión con las claves y los valores siguientes:

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  Registre el ProgID dependiente de la versión con los siguientes valores y claves:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registre el CLSID del controlador de protocolo con las claves y los valores siguientes:

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  Registre el controlador de protocolo con búsqueda en el escritorio de Windows:

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>Para registrar extensiones de Shell

Debe crear dos entradas en el registro para registrar la extensión de Shell del controlador de protocolo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




