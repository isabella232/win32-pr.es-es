---
title: Claves del Registro afectadas por WOW64
description: En WOW64, se redirigen determinadas claves del Registro.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- Claves del Registro de 64 bits Windows programación
- WOW64 64 bits de programación Windows , claves del Registro
- claves del Registro redirigidas de 64 bits Windows programación
- Claves del Registro reflejadas de 64 bits Windows programación
- Claves compartidas del Registro de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071615"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Claves del Registro afectadas por Windows que incluyen Windows en Windows (WOW) compatibilidad con varias arquitecturas de procesador

En las instalaciones de Windows de 64 bits a partir de Windows XP y Windows Server 2003, y en las instalaciones de Windows de arquitectura de procesador arm de 32 bits a partir de Windows RT (Windows 8) (a las que se hace referencia como instalaciones de **Windows** afectadas), se redirigen determinadas claves del Registro *.*

En las instalaciones de Windows afectadas, cuando un proceso con una arquitectura de procesador diferente de la arquitectura de procesador del sistema operativo (que se conoce más adelante como aplicación **WOW)** realiza una llamada del Registro para una clave redirigida, el redirector del Registro intercepta la llamada y la asigna a la ubicación del registro físico correspondiente de la clave. Por ejemplo, una aplicación Intel IA-32 x86 de 32 bits que se ejecuta en una instalación de \[  \] **AMD64** o Intel x86-x64 Windows se vería afectada por una clave del Registro redirigida; cuando esta aplicación x86 llama a una clave redirigida, el redirector del Registro intercepta la llamada de la aplicación y la redirige a la ubicación del registro físico correspondiente de la clave. Para obtener más información, vea [Redirector del Registro.](registry-redirector.md)

Otras claves del Registro *las comparten* las aplicaciones de distintas arquitecturas de procesador en las instalaciones Windows afectadas. Las llamadas del Registro de aplicaciones WOW a claves compartidas no se redirigen. En su lugar, una copia física de la clave se asigna a cada vista lógica del registro.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** También se refleja un  subconjunto de claves del Registro redirigidas para mantener sincronizadas las claves y sus valores entre las vistas de 32 y 64 bits del Registro. La reflexión del Registro se quitó a partir Windows 7 y Windows Server 2008 R2. Para obtener más información, vea [Reflexión del Registro.](registry-reflection.md)

En este tema se enumeran las claves del Registro redirigidas, compartidas o redirigidas y reflejadas en WOW. También se enumeran vínculos simbólicos que proporcionan compatibilidad para las aplicaciones existentes que pueden usar rutas de acceso de clave del Registro codificadas de forma rígida que contienen **Wow6432Node**, la ubicación del Registro redirigido para procesos x86 que se ejecutan en instalaciones de Windows AMD64. Para obtener más información, vea lo siguiente:

- [Claves redirigidas, compartidas y reflejadas en WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Windows vínculos simbólicos Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Claves redirigidas, compartidas y reflejadas en WOW

En el caso de las aplicaciones WOW Windows instalaciones afectadas, en la tabla siguiente se enumeran las claves del Registro que se redirigen, comparten o redirigen y reflejan. Las subclaves de las claves de esta tabla heredan el comportamiento de la clave primaria a menos que se especifique lo contrario. Si una clave no tiene ningún elemento primario enumerado en esta tabla, la clave se comparte.

| Clave | Windows Server 2008 R2, Windows 7 y versiones más recientes | Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP |
|-|-|-|
| **HKEY \_ LOCAL \_ MACHINE** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ CLASES \_ MACHINE\SOFTWARE** \\ **LOCALES** | Compartido | Redirigido y reflejado |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** \\ **Classes** \\ **Appid** | Compartido | Redirigidos y reflejados con una excepción: los valores del Registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía. |
| **HKEY \_ CLSID \_ de** clases \\ **DE SOFTWARE** DE MÁQUINA \\  \\ **LOCAL** | Redirected | Redirigido y reflejado solo para CLID que no especifican InprocServer32 o InprocHandler32. |
| **HKEY \_ Clases \_ DE** \\ **SOFTWARE DE** MÁQUINA LOCAL \\  \\ **DirectShow** | Redirected | Redirigido y reflejado |
| **HKEY \_ Clases \_ DE** SOFTWARE DE MÁQUINA LOCAL \\  \\  \\ **HCP** | Compartido | Compartido |
| **HKEY \_ Interfaz de \_ clases** \\ **DE SOFTWARE** \\ **DE** MÁQUINA \\ **LOCAL** | Redirected | Redirigido y reflejado |
| **HKEY \_ Tipo \_ de medio MACHINE\SOFTWARE** \\ **Classes** \\  LOCAL | Redirected | Redirigido y reflejado |
| **HKEY \_ Clases \_ de** \\ **SOFTWARE DE MÁQUINA LOCAL** \\  \\ **MediaFoundation** | Redirected | Redirigido y reflejado |
| **HKEY \_ Clientes \_ DE** \\ **SOFTWARE DE MÁQUINA** \\ **LOCAL** | Compartido | Redirected |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **COM3** | Compartido | Redirigido y reflejado |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **CryptographyCalais** \\  \\ **Current** | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Lectores** de Microsoft \\ **Cryptography** \\ **Calais** \\  | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **Cryptography** \\ **Services** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Compartido | Compartido |
| **HKEY \_ SUGERENCIA \_ DE** MICROSOFT \\  \\  \\ **CTF** DE SOFTWARE DE \\  MÁQUINA LOCAL | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **DFS** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Firma** de controladores \\  \\ **de** Microsoft | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **EnterpriseCertificates** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **EventSystem** | Compartido | Redirigido y reflejado |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **MSMQ** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Non-Driver Signing** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Bloc de notas** \\ **DefaultFonts** | Compartido | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **OLE** | Compartido | Redirigido y reflejado |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **RAS** | Compartido | Compartido |
| **HKEY \_ RPC \_ de** Microsoft \\ **DE SOFTWARE** DE MÁQUINA \\  \\ **LOCAL** | Compartido | Redirigido y reflejado |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **SOFTWARE** \\ **Microsoft** \\ **Shared Tools** \\ **MSInfo** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **SystemCertificates** | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **TermServLicensing** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **TransactionServer** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Microsoft** \\  \\ **Windows** \\ **rutas de acceso de la aplicación** \\ **CurrentVersion** | Compartido | Redirected |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** esquemas de \\  \\ **cursores Panel de control** \\  \\ **CurrentVersion** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Compartido | Redirected |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ Unidad del Explorador de \\  \\ **CurrentVersionIcons** | Compartido | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **KindMap del** \\ **Explorador** de \\ **CurrentVersion** | Compartido | Redirected |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **directiva de grupo** | Compartido | Compartido |
| **HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Compartido | Redirected |
| **HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows** programa de instalación de \\  \\ **CurrentVersion** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** ubicaciones de telefonía \\  \\  \\ **CurrentVersion** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Console**| Compartido | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Compartido | Redirected |
| **HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Fonts** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Gre \_ Initialize** | Compartido | Redirected |
| **HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Image File Execution Options** | Compartido | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Language \\ **Pack** | Compartido | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Ports** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Time Zones** | Compartido | Compartido |
| **HKEY \_ Directivas \_ DE** \\ **SOFTWARE DE MÁQUINA** \\ **LOCAL** | Compartido | Compartido |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications** | Compartido | Compartido; **Windows Server 2003 y Windows XP:** Esta clave se agregó en Windows Vista. |
| **USUARIO ACTUAL DE HKEY \_ \_** | Compartido | Compartido |
| **HKEY \_ SOFTWARE \_ DE USUARIO** \\ **ACTUAL** | Compartido | Compartido |
| **HKEY \_ Clases \_ DE** \\ **SOFTWARE DE USUARIO** \\ **ACTUAL** | Compartido | Redirigido y reflejado |
| **HKEY \_ Appid \_ de clases** \\ **DE SOFTWARE** \\ **DE** USUARIO \\ **ACTUAL** | Compartido | Redirigidos y reflejados con una excepción: los valores del Registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía. |
| **HKEY \_ CLASES \_ DE** \\ **SOFTWARE DE USUARIO** \\  \\ **ACTUAL CLSID** | Redirected | Redirigido y reflejado |
| **HKEY \_ Clases \_ DE** \\ **SOFTWARE DE** \\ **USUARIO** ACTUAL \\ **DirectShow** | Redirected | Redirigido y reflejado |
| **HKEY \_ Current \_ USER** \\ **SOFTWARE** \\ **Classes (Interfaz)** \\  | Redirected | Redirigido y reflejado |
| **HKEY \_ Current \_ USER** \\ **SOFTWARE** \\ **Classes (Tipo de** \\ **medio)** | Redirected | Redirigido y reflejado |
| **HKEY \_ Clases \_ DE** \\ **SOFTWARE DE USUARIO** \\  \\ **ACTUAL MediaFoundation** | Redirected | Redirigido y reflejado |

**HKEY \_ CURRENT \_ USER** es un vínculo simbólico al SID **\_** \\ **\[ \]** de HKEY USERS, donde SID indica una coincidencia con el identificador de seguridad \[ \] (SID) del usuario actual. **HKEY \_ USERS** \\ **\[ SID \]** \\ **SOFTWARE** \\ **Classes es** un vínculo simbólico a **HKEY \_ USERS** \\ **\[ SID \] \_ Classes**.

**HKEY \_ CLASSES \_ ROOT** es una vista combinada de **HKEY LOCAL \_ \_ MACHINE** \\ **SOFTWARE** \\ **Classes** y **HKEY CURRENT \_ \_ USER** \\ **SOFTWARE** \\ **Classes**. Las claves redirigidas en estas rutas de acceso del Registro también se redirigen de forma eficaz para **HKEY \_ CLASSES \_ ROOT.** Esto también se aplica a las claves reflejadas en los sistemas que las admiten.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows vínculos simbólicos Windows 64 (WOW64)

WOW64 define los siguientes vínculos simbólicos solo por compatibilidad con aplicaciones existentes que pueden usar rutas de acceso de clave del Registro codificadas de forma rígida que contienen Wow6432Node. Las nuevas aplicaciones deben evitar el uso de Wow6432Node en las rutas de acceso de la clave del Registro.

- **HKEY \_ Las \_ clases \\ \\ WOW6432Node \\** de LOCAL MACHINE SOFTWARE están vinculadas a **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**
- **HKEY \_ Las clases DE SOFTWARE DE MÁQUINA LOCAL \_ \\ \\ \\ Wow6432Node \\ AppId** están vinculadas a **HKEY \_ LOCAL MACHINE SOFTWARE \_ Classes \\ \\ \\ AppId**
- **HKEY \_ Las clases DE SOFTWARE DE MÁQUINA LOCAL \_ \\ \\ \\ Wow6432Node \\ PROTOCOLS** están vinculadas **a HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ PROTOCOLS**
- **HKEY \_ Las \_ clases DE SOFTWARE DE MÁQUINA LOCAL \\ \\ \\ Wow6432Lib \\ de nodos** están vinculadas a la biblioteca de tipos **HKEY LOCAL MACHINE SOFTWARE \_ \_ \\ \\ Classes \\**

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP: HKEY \_ Las \_ clases \\ \\ WOW6432Node \\** de LOCAL MACHINE SOFTWARE están vinculadas a **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**. Se agregaron otros vínculos simbólicos en Windows 7 y Windows Server 2008 R2.
