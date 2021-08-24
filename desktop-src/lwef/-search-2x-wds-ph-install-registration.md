---
title: Instalación y registro de controladores de protocolo (características heredadas Windows entorno)
description: La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio Archivos de programa y registrarlos.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716565"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Instalación y registro de controladores de protocolo (características heredadas Windows entorno)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

La **instalación de controladores de** protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio Archivos de programa y registrarlos.

Esta sección contiene los siguientes temas:

-   [Instrucciones de instalación](#installation-guidelines)
-   [Para registrar controladores de protocolo](#to-register-protocol-handlers)
-   [Para registrar extensiones de shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Instrucciones de instalación

Los controladores de protocolos deben implementar el registro propio para la instalación y deben seguir estas directrices:

-   El instalador debe usar el instalador EXE o MSI.
-   Se deben proporcionar notas de la versión.
-   Se **debe crear una entrada Agregar** o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.
-   Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debe haber la capacidad de restaurar la funcionalidad del complemento anterior y convertirla de nuevo en el complemento predeterminado para ese tipo de archivo.

## <a name="to-register-protocol-handlers"></a>Para registrar controladores de protocolo

Debe realizar decimocuartos entradas en el Registro para registrar el componente de controlador de protocolo, donde:

-   *Ver \_ Ind \_ ProgID es* el ProgID independiente de la versión de la implementación del controlador de protocolo.
-   *Ver \_ Dep \_ ProgID es* el ProgID dependiente de la versión de la implementación del controlador de protocolo.
-   *CLSID \_ 1 es* el CLSID de la implementación del controlador de protocolo

1.  Registre el ProgID independiente de la versión con las siguientes claves y valores:

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

2.  Registre el ProgID dependiente de la versión con las siguientes claves y valores:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registre el CLSID del controlador de protocolo con las siguientes claves y valores:

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

4.  Registre el controlador de protocolo con Windows Desktop Search:

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

## <a name="to-register-shell-extensions"></a>Para registrar extensiones de shell

Debe crear dos entradas en el Registro para registrar la extensión shell del controlador de protocolo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




