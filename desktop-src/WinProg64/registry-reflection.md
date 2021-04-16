---
title: Reflexión del registro
description: El redirector del registro aísla las aplicaciones de 32 y 64 bits proporcionando vistas lógicas independientes de ciertas partes del registro en WOW64. Sin embargo, los valores de algunas claves del registro deben ser los mismos en las vistas de 32 bits y de 64 bits.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- reflexión del registro 64 programación de Windows de bits
- Reflection 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695682"
---
# <a name="registry-reflection"></a>Reflexión del registro

\[La información de este tema se aplica a Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP. A partir de Windows 7 y Windows Server 2008 R2, WOW64 ya no utiliza la reflexión del registro y, en su lugar, se comparten claves reflejadas. Para obtener más información, consulte [claves del registro afectadas por WOW64](shared-registry-keys.md).\]

El [redirector del registro](registry-redirector.md) aísla las aplicaciones de 32 y 64 bits proporcionando vistas lógicas independientes de ciertas partes del registro en WOW64. Sin embargo, los valores de algunas claves del registro deben ser los mismos en las vistas de 32 bits y de 64 bits.

El proceso de *reflexión del registro* copia las claves y los valores del registro entre dos vistas del registro para mantenerlas sincronizadas. Cada vista tiene una copia física independiente de cada clave del registro reflejada, una para la vista del registro de 32 bits y la otra para la vista del registro de 64 bits.

Cuando se cierra una clave mediante una llamada a [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey), se copia una clave reflejada. Tenga en cuenta que esto da lugar a una posible condición de carrera: Si más de un proceso cambia la clave reflejada, la última llamada a **RegCloseKey** determina el valor final de la clave.

El reflector copia los datos de activación COM para los servidores locales entre las vistas, pero no copia los datos en proceso porque 32/64 no se permite la combinación de datos en proceso en Windows de 64 bits.

La reflexión no está habilitada para las claves del registro compartidas o para las claves del registro que no se redirigen. Por ejemplo, la reflexión no está habilitada para la clave **\_ \_ \\ del sistema del equipo local HKEY** . Para obtener una lista de las claves del registro que se redirigen, comparten o reflejan, consulte [las claves del registro afectadas por WOW64](shared-registry-keys.md).

La reflexión del registro utiliza una directiva de "último escritor WINS" como se muestra en el ejemplo siguiente:

-   Después de una instalación limpia de Windows de 64 bits, el Wordpad.exe de 64 bits se registra para administrar los archivos. doc. El reflector copia el registro. doc de la vista del registro de 64 bits en la vista del registro de 32 bits.
-   Un administrador instala Office de 32 bits, que registra Winword.exe de 32 bits para administrar los archivos. doc en la vista del registro de 32 bits. El reflector del registro copia esta información en la vista del registro de 64 bits, por lo que las aplicaciones de 32 bits y de 64 bits inician la versión de 32 bits de Winword.exe para los archivos. doc.
-   Un administrador instala Office de 64 bits, que registra Winword.exe de 64 bits para administrar los archivos. doc en la vista del registro de 64 bits. El reflector del registro copia esta información en el registro de 32 bits, por lo que las aplicaciones de 32 bits y de 64 bits inician la versión de 64 bits de Winword.exe para los archivos. doc.

Por lo tanto, se conserva la información de Asociación de archivos para la aplicación instalada más recientemente.

Puede ser útil para que las aplicaciones de 32 bits y 64 bits compartan valores de clave del registro específicos que normalmente se escriben en vistas del registro independientes. Por ejemplo, un servidor OLE de 32 bits que puede atender solicitudes de clientes de 32 bits y de 64 bits podría hacer que los datos del registro de 32 bits estén disponibles para la vista de 64 bits del registro del sistema.

Cuando un componente escribe datos en el registro del sistema, WOW64 analiza la información y realiza una copia de los datos en la vista alternativa del registro cuando sea necesario. Normalmente, este proceso mantiene dos copias físicas independientes de las mismas claves del registro en ambas vistas del registro y se denomina reflexión de registro o reflejo de registro.

La mayoría de las claves de la raíz de las clases están en esta categoría. Las actualizaciones de las claves se reflejan cuando se completa la actualización y se cierra el identificador de la clave. En casos concretos, las operaciones de escritura en una clave no se reflejan si la clave tiene una dependencia de varios bits. Por ejemplo, la clave InprocServer32 de 32 bits no es relevante para las aplicaciones de 64 bits, por lo que la clave InprocServer32 no se refleja en la vista del registro de 64 bits. Sin embargo, las aplicaciones de 64 bits pueden usar la clave LocalServer32 de 32 bits y la clave LocalServer32 se refleja.

En el caso de **\_ \_ \\ \\ las clases \\ de software de máquina local de HKEY CLSID** y **HKEY clases de software de \_ \_ usuario actuales \\ \\ \\ CLSID**, solo se reflejan los CLSID que no especifican InProcServer32 o InprocHandler32. Solo se reflejan los CLSID de LocalServer32 porque se ejecutan fuera de proceso y se pueden activar mediante aplicaciones de 32 o 64 bits. Los CLSID de InProcServer32 no se reflejan porque no es posible cargar un archivo DLL de 32 bits para su ejecución en un proceso de 64 bits o un archivo DLL de 64 bits para su ejecución en un proceso de 32 bits.

En el caso de **\_ \_ \\ \\ las clases \\ de software de máquina local de HKEY AppID** y **HKEY clases de software de \_ \_ usuario actuales \\ \\ \\ AppID**, los valores del registro [DllSurrogate](../com/dllsurrogate.md) y [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) no se reflejan si su valor es una cadena vacía.

Para deshabilitar y habilitar la reflexión del registro para una clave reflejada determinada, use las funciones [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) y [**RegEnableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) . Estas funciones no afectan a las claves que no están en la lista de claves reflejadas anteriormente en este tema. Las aplicaciones solo deben deshabilitar la reflexión para las claves del registro que crean y no intentan deshabilitar la reflexión para las claves predefinidas como **HKEY \_ local \_ Machine** o **HKEY \_ Current \_ User**. Para determinar si se han deshabilitado las claves de la lista de reflexión, utilice la función [**RegQueryReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) .

Las claves reflejadas no deben usarse en operaciones del registro transaccionales. La escritura en claves reflejadas durante una transacción puede provocar un error en la transacción. Para obtener más información acerca de las transacciones, consulte [Administrador de transacciones de kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del registro](registry-redirector.md)
</dt> <dt>

[Reflexión del registro en Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Claves del Registro afectadas por WOW64](shared-registry-keys.md)
</dt> </dl>

 

 