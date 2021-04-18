---
title: Claves del Registro afectadas por WOW64
description: Bajo WOW64, se redirigen ciertas claves del registro.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- claves del registro de la programación de Windows de 64 bits
- WOW64 64 bits programación de Windows, claves del registro
- 'claves del registro redirigidas: programación de Windows de 64 bits'
- claves del registro reflejadas programación de Windows de 64 bits
- claves del registro compartidas programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48278bfd42656b05d0e1f2be4402496a873022d1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105717323"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Claves del registro afectadas por las instalaciones de Windows que incluyen compatibilidad con Windows on Windows (WOW) para varias arquitecturas de procesador

En las instalaciones de Windows de 64 bits a partir de Windows XP y Windows Server 2003, y en la arquitectura de procesador ARM de 32 bits de las instalaciones de Windows a partir de Windows RT (Windows 8) (a partir de ahora, se hace referencia a ellas como **instalaciones de Windows afectadas**), se *redirigen* ciertas claves del registro.

En las instalaciones de Windows afectadas, cuando un proceso con una arquitectura de procesador diferente de la arquitectura del procesador del sistema operativo (lo que se conoce como una **aplicación wow**) realiza una llamada al registro para una clave redirigida, el redirector del registro intercepta la llamada y la asigna a la ubicación del registro física correspondiente de la clave. Por ejemplo, una aplicación Intel IA-32 x86 de 32 bits \[  \] que se ejecuta en una instalación de Windows de **AMD64** /Intel x86-x64 se vería afectada por una clave del registro Redirigido; cuando esta aplicación x86 llama a una clave redirigida, el redirector del registro intercepta la llamada de la aplicación y la redirige a la ubicación del registro física correspondiente de la clave. Para obtener más información, vea [redirector del registro](registry-redirector.md).

Las aplicaciones de distintas arquitecturas de procesador *comparten* otras claves del registro en las instalaciones de Windows afectadas. Las llamadas del registro de la aplicación WOW a claves compartidas no se redirigen. En su lugar, se asigna una copia física de la clave a cada vista lógica del registro.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** También se *refleja* un subconjunto de claves del registro redirigidas para mantener sincronizadas las claves y sus valores entre las vistas de 32 bits y 64 bits del registro. La reflexión del registro se quitó a partir de Windows 7 y Windows Server 2008 R2. Para obtener más información, vea [reflexión del registro](registry-reflection.md).

En este tema se enumeran las claves del registro que se redirigen, comparten o redirigen en WOW. También se enumeran los vínculos simbólicos que proporcionan compatibilidad con las aplicaciones existentes que pueden utilizar rutas de acceso de clave del registro codificadas que contienen **Wow6432Node**, la ubicación del registro redirigido para los procesos x86 que se ejecutan en instalaciones de Windows AMD64. Para obtener más información, vea lo siguiente:

- [Claves redirigidas, compartidas y reflejadas en WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Vínculos simbólicos de Windows en Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Claves redirigidas, compartidas y reflejadas en WOW

En el caso de las aplicaciones WOW en las instalaciones de Windows afectadas, en la tabla siguiente se enumeran las claves del registro redirigidas, compartidas o redirigidas y reflejadas. Las subclaves de las claves de esta tabla heredan el comportamiento de la clave principal, a menos que se especifique lo contrario. Si una clave no tiene ningún elemento primario enumerado en esta tabla, la clave se comparte.

| Clave | Windows Server 2008 R2, Windows 7 y versiones más recientes | Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP |
|-|-|-|
| **HKEY \_ local \_ Machine** | Compartido | Compartido |
| **HKEY \_ local \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ Clases \_ MACHINE\SOFTWARE locales** \\  | Compartido | Redirigido y reflejado |
| **HKEY \_ Clases \_ MACHINE\SOFTWARE locales** \\  \\ **AppID** | Compartido | Redirigido y reflejado con una excepción: los valores del registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía. |
| **HKEY \_ \_** Clases de \\ **software** de equipo local \\  \\ **CLSID** | Redirected | Se redirige y refleja solo para CLSID que no especifican InprocServer32 ni InprocHandler32. |
| **HKEY \_ \_** Clases de \\ **software** de máquina local \\  \\ **DirectShow** | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Clases de \\ **software** de máquina local \\  \\ **HCP** | Compartido | Compartido |
| **HKEY \_ \_** Interfaz de \\  \\ **clases** \\  de software de máquina local | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Tipo de \\  \\ **medio** de clases MACHINE\SOFTWARE locales | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Clases de \\ **software** de equipo local \\  \\ **MediaFoundation** | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Clientes de \\ **software** \\  de máquina local | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **COM3** | Compartido | Redirigido y reflejado |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **actual** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **Readers** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **Services** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **CTF** \\ **Tip** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **DFS** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** firma de \\  \\  \\ **Controladores** de Microsoft | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **EnterpriseCertificates** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **EventSystem** | Compartido | Redirigido y reflejado |
| **HKEY \_ SOFTWARE de \_ máquina local** \\  \\ **Microsoft** \\ **MSMQ** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\  \\ **: firma de Microsoft sin controlador** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Notepad** \\ **DefaultFonts** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **OLE** | Compartido | Redirigido y reflejado |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **ras** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **RPC** | Compartido | Redirigido y reflejado |
| **HKEY \_ Software de \_ equipo local** software de \\  \\ **Microsoft** \\  \\ **Microsoft** \\ **herramientas compartidas** \\ **Msinfo** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **SystemCertificates** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **TermServLicensing** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **TransactionServer** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **controles** de \\ **cursores** \\  del panel de control | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Directiva de grupo** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **setup** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telephony** \\ **locations** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Console**| Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Fonts** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **GRE \_ Initialize** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ paquete de idioma de **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  | Compartido | Redirected |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ports** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Compartido | Compartido |
| **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Time Zones** | Compartido | Compartido |
| **HKEY \_ \_** Directivas de \\ **software** \\  de máquina local | Compartido | Compartido |
| **HKEY \_ \_** RegisteredApplications de \\ **software** \\  de equipo local | Compartido | Recurso **Windows Server 2003 y Windows XP:** Esta clave se agregó en Windows Vista. |
| **HKEY \_ Current \_ User** | Compartido | Compartido |
| **HKEY \_ SOFTWARE del \_ usuario actual** \\  | Compartido | Compartido |
| **HKEY \_ \_** Clases de \\ **software** \\  de usuario actuales | Compartido | Redirigido y reflejado |
| **HKEY \_ \_** Clases de \\ **software** de usuario actuales \\  \\ **AppID** | Compartido | Redirigido y reflejado con una excepción: los valores del registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía. |
| **HKEY \_ \_** Clases de \\ **software** de usuario actuales \\  \\ **CLSID** | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Clases de \\ **software** de usuario actuales \\  \\ **DirectShow** | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Interfaz de \\  \\ **clases** \\  de software de usuario actual | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Tipo de \\  \\  \\ **medio** de clases de software de usuario actual | Redirected | Redirigido y reflejado |
| **HKEY \_ \_** Clases de \\ **software** de usuario actual \\  \\ **MediaFoundation** | Redirected | Redirigido y reflejado |

**HKEY \_ El \_ usuario actual** es un vínculo simbólico al SID **\_** \\ **\[ \]** de los usuarios HKEY donde \[ SID \] indica una coincidencia para el ID. de seguridad (SID) del usuario actual. **HKEY \_ Users** \\ **\[ SID \]** \\  \\ **classes** es un vínculo simbólico **a \_** \\ **\[ \] \_ clases de SID** de usuario HKEY.

**HKEY \_ La \_ raíz de las clases** es una vista combinada de las clases de software del **\_ \_ equipo local HKEY** \\  \\  y de las clases de software de **\_ \_ usuario actuales** \\  \\ . Las claves redirigidas en estas rutas de acceso del registro se redirigen realmente para **\_ las clases HKEY \_ raíz** también. Esto también se aplica a las claves reflejadas en los sistemas que las admiten.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Vínculos simbólicos de Windows en Windows 64 (WOW64)

WOW64 define los siguientes vínculos simbólicos únicamente para la compatibilidad con las aplicaciones existentes que pueden utilizar rutas de acceso de clave del registro codificadas que contienen Wow6432Node. Las nuevas aplicaciones deben evitar el uso de Wow6432Node en las rutas de acceso de clave del registro.

- **HKEY \_ \_ \\ \\ \\ Las clases de software WOW6432NODE de la máquina local** están vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**
- **HKEY \_ \_Clases de software de equipo local \\ \\ \\ Wow6432Node \\ AppID** está vinculada a **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID**
- **HKEY \_ \_Clases de software de equipo local \\ \\ \\ Wow6432Node \\ protocolos** está vinculado a **HKEY \_ local \_ Machine \\ software \\ classes \\ Protocols**
- **HKEY \_ \_Clases de software de equipo local \\ \\ \\ Wow6432Node \\ typelib** está vinculado a **HKEY \_ local \_ Machine \\ software \\ classes \\ typelib**

**Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP: HKEY \_ \_ \\ \\ \\ Las clases de software WOW6432NODE de la máquina local** están vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**. Se han agregado otros vínculos simbólicos en Windows 7 y Windows Server 2008 R2.
