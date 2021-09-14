---
title: Reflexión del Registro
description: El redirector del registro aísla aplicaciones de 32 y 64 bits al proporcionar vistas lógicas independientes de determinadas partes del registro en WOW64. Sin embargo, los valores de algunas claves del Registro deben ser los mismos en las vistas de 32 y 64 bits.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- Reflexión del registro de 64 bits Windows programación
- reflexión de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073115"
---
# <a name="registry-reflection"></a>Reflexión del Registro

\[La información de este tema se aplica a Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP. A partir de Windows 7 y Windows Server 2008 R2, WOW64 ya no usa la reflexión del Registro y, en su lugar, se comparten las claves reflejadas anteriormente. Para obtener más información, vea [Claves del Registro afectadas por WOW64.](shared-registry-keys.md)\]

El [redirector del registro](registry-redirector.md) aísla aplicaciones de 32 y 64 bits al proporcionar vistas lógicas independientes de determinadas partes del registro en WOW64. Sin embargo, los valores de algunas claves del Registro deben ser los mismos en las vistas de 32 y 64 bits.

El proceso de *reflexión del Registro* copia las claves y los valores del Registro entre dos vistas del Registro para mantenerlas sincronizadas. Cada vista tiene una copia física independiente de cada clave del Registro reflejada, una para la vista del Registro de 32 bits y la otra para la vista del Registro de 64 bits.

Una clave reflejada se copia cuando se cierra una clave mediante una [**llamada a RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey). Tenga en cuenta que esto da lugar a una posible condición de carrera: si más de un proceso cambia la clave reflejada, la última llamada **RegCloseKey** determina el valor final de la clave.

El reflector copia los datos de activación COM para los servidores locales entre las vistas, pero no copia los datos en proceso porque no se permite la combinación de datos en proceso de 32/64 en las vistas de 64 Windows.

La reflexión no está habilitada para las claves del Registro compartidas o para las claves del Registro que no se redirigen. Por ejemplo, la reflexión no está habilitada para la clave **HKEY \_ LOCAL MACHINE \_ \\ System.** Para obtener una lista de claves del Registro redirigidas, compartidas o reflejadas, vea Claves del Registro [afectadas por WOW64.](shared-registry-keys.md)

La reflexión del Registro usa una directiva "el último escritor gana", como se muestra en el ejemplo siguiente:

-   Después de una instalación limpia de archivos de 64 Windows, las Wordpad.exe de 64 bits se registran para controlar .doc archivos. El reflector copia el registro .doc de la vista del Registro de 64 bits en la vista del Registro de 32 bits.
-   Un administrador instala Office de 32 bits, que registra archivos de Winword.exe de 32 bits para controlar .doc archivos en la vista del Registro de 32 bits. El reflector del Registro copia esta información en la vista del Registro de 64 bits, por lo que tanto las aplicaciones de 32 bits como las de 64 bits inician la versión de 32 bits de Winword.exe para .doc archivos.
-   Un administrador instala un Office de 64 bits, que registra Winword.exe de 64 bits para controlar .doc archivos en la vista del Registro de 64 bits. El reflector del Registro copia esta información en el registro de 32 bits, por lo que tanto las aplicaciones de 32 bits como las de 64 bits inician la versión de 64 bits de Winword.exe para .doc archivos.

Por lo tanto, la información de asociación de archivos se conserva para la aplicación instalada más recientemente.

Puede ser útil para las aplicaciones de 32 y 64 bits compartir valores de clave del Registro específicos que normalmente se escriben en vistas del Registro independientes. Por ejemplo, un servidor OLE de 32 bits que pueda atender solicitudes de clientes de 32 y 64 bits podría hacer que sus datos del Registro de 32 bits estén disponibles para la vista de 64 bits del registro del sistema.

Cuando un componente escribe datos en el registro del sistema, WOW64 analiza la información y realiza una copia de los datos en la vista alternativa del registro cuando corresponda. Normalmente, este proceso mantiene dos copias físicas independientes de las mismas claves del Registro en ambas vistas del Registro y se denomina reflexión del Registro o creación de reflejo del Registro.

La mayoría de las claves de la raíz de clases están en esta categoría. Las actualizaciones de las claves se reflejan cuando se completa la actualización y se cierra el identificador de la clave. En casos específicos, las escrituras en una clave no se reflejan si la clave tiene alguna dependencia de bits. Por ejemplo, la clave InprocServer32 de 32 bits no es relevante para las aplicaciones de 64 bits, por lo que la clave InprocServer32 no se refleja en la vista del Registro de 64 bits. Sin embargo, las aplicaciones de 64 bits pueden usar la clave LocalServer32 de 32 bits y la clave LocalServer32 se refleja.

Para las clases de **\_ software HKEY LOCAL MACHINE \_ \\ \\ \\ CLSID** y **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID**, solo se reflejan los CLID que no especifican InprocServer32 o InprocHandler32. Solo se reflejan los CLID LocalServer32 porque se ejecutan fuera de proceso y pueden activarse mediante aplicaciones de 32 o 64 bits. Los CLID inProcServer32 no se reflejan porque no es posible cargar un archivo DLL de 32 bits para su ejecución en un proceso de 64 bits o un archivo DLL de 64 bits para su ejecución en un proceso de 32 bits.

Para las clases de **\_ software HKEY LOCAL MACHINE \_ \\ \\ \\ Appid** y **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ Appid**, los valores del Registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía.

Para deshabilitar y habilitar la reflexión del Registro para una clave reflejada determinada, use las funciones [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) y [**RegEnableReflectionKey.**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) Estas funciones no afectan a las claves que no están en la lista de claves reflejadas anteriormente en este tema. Las aplicaciones deben deshabilitar la reflexión solo para las claves del Registro que crean y no intentar deshabilitar la reflexión para las claves predefinidas, como **HKEY \_ LOCAL \_ MACHINE** o **HKEY \_ CURRENT \_ USER**. Para determinar si se han deshabilitado las claves de la lista de reflexión, use la [**función RegQueryReflectionKey.**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey)

Las claves reflejadas no deben usarse en operaciones del Registro con transacciones. Escribir en claves reflejadas durante una transacción puede provocar un error en la transacción. Para obtener más información sobre las transacciones, vea [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del Registro](registry-redirector.md)
</dt> <dt>

[Reflexión del Registro en Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Claves del Registro afectadas por WOW64](shared-registry-keys.md)
</dt> </dl>

 

 