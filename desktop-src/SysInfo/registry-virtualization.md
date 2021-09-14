---
description: La virtualización del registro es una tecnología de compatibilidad de aplicaciones que permite redirigir las operaciones de escritura del registro que tienen un impacto global a ubicaciones por usuario.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualización del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160683"
---
# <a name="registry-virtualization"></a>Virtualización del registro

*La virtualización del* registro es una tecnología de compatibilidad de aplicaciones que permite redirigir las operaciones de escritura del registro que tienen un impacto global a ubicaciones por usuario. Este redireccionamiento es transparente para las aplicaciones que leen o escriben en el Registro. Se admite a partir de Windows Vista.

Esta forma de virtualización es una tecnología de compatibilidad provisional de aplicaciones. Microsoft pretende quitarlo de versiones futuras del sistema operativo Windows, ya que hay más aplicaciones compatibles con Windows Vista y versiones posteriores de Windows. Por lo tanto, es importante que la aplicación no dependa del comportamiento de la virtualización del registro en el sistema.

La virtualización está pensada únicamente para proporcionar compatibilidad con las aplicaciones existentes. Las aplicaciones diseñadas para Windows Vista y versiones posteriores de Windows no deben escribir en áreas del sistema confidenciales ni deben basarse en la virtualización para solucionar problemas. Al actualizar el código existente para que se ejecute en Windows Vista y versiones posteriores de Windows, los desarrolladores deben asegurarse de que las aplicaciones solo almacenan datos en ubicaciones por usuario o en ubicaciones de equipo dentro de %alluserprofile% que usan correctamente una lista de control de acceso (ACL).

Para obtener más información sobre la creación de aplicaciones compatibles con UAC, consulte la [Guía para desarrolladores de UAC](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Información general sobre virtualización

Antes de Windows Vista, los administradores normalmente ejecutaban las aplicaciones. Como resultado, las aplicaciones podrían acceder libremente a los archivos del sistema y las claves del Registro. Si un usuario estándar ejecutara estas aplicaciones, se produciría un error debido a derechos de acceso insuficientes. Windows Vista y versiones posteriores de Windows compatibilidad de aplicaciones para estas aplicaciones mediante la redirección automática de estas operaciones. Por ejemplo, las operaciones del Registro al almacén global **(HKEY \_ LOCAL \_ MACHINE \\ Software**) se redirigen a una ubicación por usuario dentro del perfil del usuario conocida como *almacén virtual* (**HKEY USERS Classes \_ \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software**).

La virtualización del registro se puede clasificar ampliamente en los siguientes tipos:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Open Registry Virtualization
</dt> <dd>

Si el autor de la llamada no tiene acceso de escritura a una clave e intenta abrirla, la clave se abre con el acceso máximo permitido para ese autor de la llamada.

Si se establece la marca REG KEY DONT SILENT FAIL para la clave, se produce un error en la operación y \_ no se abre la \_ \_ \_ clave. Para obtener más información, vea "Control de la virtualización del registro" más adelante en este tema.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Escritura de la virtualización del registro
</dt> <dd>

Si el autor de la llamada no tiene acceso de escritura a una clave e intenta escribir un valor en ella o crear una subclave, el valor se escribe en el almacén virtual.

Por ejemplo, si un usuario limitado intenta escribir un valor en la clave **siguiente: HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1 , la virtualización redirige la operación de escritura a \\  **HKEY USERS \_ Classes \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lee la virtualización del registro.
</dt> <dd>

Si el autor de la llamada lee de una clave virtualizada, el Registro presenta una vista combinada de los valores virtualizados (del almacén virtual) y los valores no virtuales (del almacén global) al autor de la llamada.

Por ejemplo, suponga **que HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1 contiene dos valores V1 y V2 y que un usuario limitado escribe un valor \\  V3 en la clave. Cuando el usuario intenta leer valores de esta clave, la vista combinada incluye los valores V1 y V2 del almacén global y el valor V3 del almacén virtual.

Tenga en cuenta que los valores virtuales tienen prioridad sobre los valores globales cuando están presentes. En el ejemplo anterior, incluso si el almacén global tuviera el valor V3 bajo esta clave, el valor V3 todavía se devolvería al autor de la llamada desde el almacén virtual. Si V3 se eliminara del almacén virtual, la versión 3 se devolvería del almacén global. En otras palabras, si V3 se eliminara de las clases **HKEY \_ USERS \\ <User SID> \_ \\ \\ \\ VirtualStore Machine Software** \\ *AppKey1* pero **HKEY LOCAL MACHINE \_ \_ \\ Software** \\ *AppKey1* tuviera un valor V3, ese valor se devolvería del almacén global.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Ámbito de virtualización del registro

La virtualización del Registro solo está habilitada para lo siguiente:

-   Procesos interactivos de 32 bits.
-   Claves en **HKEY \_ LOCAL MACHINE \_ \\ Software**.
-   Claves en las que un administrador puede escribir. (Si un administrador no puede escribir en una clave, la aplicación habría fallado en versiones anteriores de Windows incluso si lo ejecutara un administrador).

La virtualización del Registro está deshabilitada para lo siguiente:

-   Procesos de 64 bits.
-   Procesos que no son interactivos, como los servicios.

    Tenga en cuenta que el uso del Registro como mecanismo de comunicación entre procesos (IPC) entre un servicio (o cualquier otro proceso que no tenga habilitada la virtualización) y una aplicación no funcionará correctamente si la clave está virtualizada. Por ejemplo, si un servicio antivirus actualiza sus archivos de firma en función de un valor establecido por una aplicación, el servicio nunca actualizará sus archivos de firma porque el servicio lee desde el almacén global, pero la aplicación escribe en el almacén virtual.

-   Procesos que suplantan a un usuario. Si un proceso intenta realizar una operación al suplantar a un usuario, esa operación no se virtualizará.
-   Procesos en modo kernel, como controladores.
-   Procesos que han **solicitadoExecutionLevel** especificado en sus manifiestos.
-   Claves y subclaves de las clases **de software HKEY \_ LOCAL \_ MACHINE \\ \\**, **HKEY LOCAL MACHINE Software \_ \_ Microsoft \\ \\ \\ Windows** y **HKEY LOCAL MACHINE Software \_ Microsoft Windows \_ \\ \\ \\ NT**.

## <a name="controlling-registry-virtualization"></a>Control de la virtualización del registro

Además de controlar la virtualización en un nivel de aplicación mediante **requestedExecutionLevel** en el **\_ \_ \\ manifiesto,** un administrador puede habilitar o deshabilitar la virtualización por clave para las claves de HKEY LOCAL MACHINE Software . Para ello, use la Reg.exe de línea de comandos FLAGS con las marcas enumeradas en la tabla siguiente.



| Marca                         | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ SILENCIOSO DE LA CLAVE \_ REG \_ \_ | Esta marca deshabilita la virtualización abierta del registro. Si se establece esta marca y se produce un error en una operación abierta en una clave que tiene habilitada la virtualización, el Registro no intenta volver a abrir la clave. Si esta marca está clara, el Registro intenta volver a abrir la clave con el acceso MÁXIMO PERMITIDO \_ en lugar del acceso solicitado.                                                                   |
| NO \_ VIRTUALIZAR \_ CLAVE REG \_   | Esta marca deshabilita la virtualización del registro de escritura. Si se establece esta marca y se produce un error en una operación de creación de clave o valor establecido porque el autor de la llamada no tiene suficiente acceso a la clave primaria, el Registro produce un error en la operación. Si esta marca está clara, el Registro intenta escribir la clave o el valor en el almacén virtual. El autor de la llamada debe tener el derecho \_ KEY READ en la clave primaria. |
| REG \_ KEY \_ RECURSE \_ FLAG      | Si se establece esta marca, las marcas de virtualización del Registro se propagan desde la clave primaria. Si esta marca está clara, las marcas de virtualización del registro no se propagan. El cambio de esta marca solo afecta a las nuevas claves descendientes creadas después de cambiar la marca. No establece ni borra estas marcas para las claves descendientes existentes.                                                                  |



 

En el ejemplo siguiente se muestra el uso de la utilidad de línea de comandos Reg.exe con la opción FLAGS para consultar el estado de las marcas de virtualización para obtener una clave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Cada vez que se habilita la auditoría en una clave que se virtualiza, se genera un nuevo evento de auditoría de virtualización para indicar que la clave se está virtualizar (además de los eventos de auditoría habituales). Los administradores pueden usar esta información para supervisar el estado de virtualización en sus sistemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales control de cuentas de usuario](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Descripción y configuración del control de cuentas de usuario](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Procedimientos recomendados y directrices para desarrolladores para aplicaciones en un entorno con privilegios mínimos](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
