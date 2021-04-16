---
description: La virtualización del registro es una tecnología de compatibilidad de aplicaciones que permite realizar operaciones de escritura en el registro que tienen un impacto global en las ubicaciones por usuario.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualización del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669965"
---
# <a name="registry-virtualization"></a>Virtualización del registro

La *virtualización del registro* es una tecnología de compatibilidad de aplicaciones que permite realizar operaciones de escritura en el registro que tienen un impacto global en las ubicaciones por usuario. Esta redirección es transparente para las aplicaciones que leen o escriben en el registro. Se admite a partir de Windows Vista.

Esta forma de virtualización es una tecnología provisional de compatibilidad de aplicaciones; Microsoft tiene la intención de quitarlo de versiones futuras del sistema operativo Windows a medida que haya más aplicaciones compatibles con Windows Vista y versiones posteriores de Windows. Por lo tanto, es importante que la aplicación no dependa del comportamiento de la virtualización del registro en el sistema.

La virtualización está destinada únicamente a proporcionar compatibilidad para las aplicaciones existentes. Las aplicaciones diseñadas para Windows Vista y versiones posteriores de Windows no deben escribir en áreas del sistema confidenciales, ni deben basarse en la virtualización para solucionar los problemas. Al actualizar el código existente para que se ejecute en Windows Vista y versiones posteriores de Windows, los desarrolladores deben asegurarse de que las aplicaciones solo almacenan datos en ubicaciones por usuario o en ubicaciones de equipos dentro del% alluserprofile% que usan correctamente una lista de control de acceso (ACL).

Para obtener más información acerca de la creación de aplicaciones compatibles con UAC, vea la [Guía para desarrolladores de UAC](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Información general de virtualización

Antes de Windows Vista, los administradores normalmente ejecutaban las aplicaciones. Como resultado, las aplicaciones pueden acceder libremente a los archivos del sistema y las claves del registro. Si estas aplicaciones fueron ejecutadas por un usuario estándar, se producirían errores debido a derechos de acceso insuficientes. Windows Vista y versiones posteriores de Windows mejoran la compatibilidad de aplicaciones para estas aplicaciones mediante la redirección automática de estas operaciones. Por ejemplo, las operaciones del registro en el almacén global (**HKEY \_ local \_ Machine \\ software**) se redirigen a una ubicación por usuario en el perfil del usuario conocido como el *almacén virtual* (**HKEY \_ users \\ <User SID> \_ classes \\ VirtualStore \\ Machine \\ software**).

La virtualización del registro se puede clasificar ampliamente en los siguientes tipos:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Abrir la virtualización del registro
</dt> <dd>

Si el autor de la llamada no tiene acceso de escritura a una clave e intenta abrir la clave, la clave se abre con el acceso máximo permitido para ese llamador.

Si \_ \_ \_ se establece la marca de no silenciosa de la clave \_ de registro para la clave, se produce un error en la operación y no se abre la clave. Para obtener más información, vea "controlar la virtualización del registro" más adelante en este tema.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Escribir la virtualización del registro
</dt> <dd>

Si el autor de la llamada no tiene acceso de escritura a una clave e intenta escribir un valor en él o crear una subclave, el valor se escribe en el almacén virtual.

Por ejemplo, si un usuario limitado intenta escribir un valor en la clave siguiente: **HKEY \_ local \_ Machine \\ software** \\ *AppKey1*, Virtualization redirige la operación de escritura a **\_ las clases HKEY users \\ <User SID> \_ \\ VirtualStore \\ Machine \\ software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Leer la virtualización del registro
</dt> <dd>

Si el autor de la llamada Lee una clave que está virtualizada, el registro presenta una vista combinada de los valores virtualizados (del almacén virtual) y los valores no virtuales (del almacén global) al autor de la llamada.

Por ejemplo, supongamos que **HKEY \_ local \_ Machine \\ software** \\ *AppKey1* contiene dos valores V1 y V2 y que un usuario limitado escribe un valor V3 en la clave. Cuando el usuario intenta leer valores de esta clave, la vista combinada incluye los valores V1 y V2 del almacén global y el valor V3 del almacén virtual.

Tenga en cuenta que los valores virtuales tienen prioridad sobre los valores globales cuando están presentes. En el ejemplo anterior, aunque el almacén global tuviera el valor V3 en esta clave, el valor V3 se seguiría devolviendo al llamador desde el almacén virtual. Si V3 debía eliminarse del almacén virtual, se devolvería V3 desde el almacén global. En otras palabras, si V3 se eliminara de **HKEY \_ users \\ <User SID> \_ classes \\ VirtualStore \\ Machine \\ software** \\ *AppKey1* , pero **HKEY \_ local \_ Machine \\ software** \\ *AppKey1* tenía un valor V3, ese valor se devolvería desde el almacén global.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Ámbito de virtualización del registro

La virtualización del registro solo está habilitada para lo siguiente:

-   procesos interactivos de 32 bits.
-   Claves en **el \_ \_ \\ software de máquina local HKEY**.
-   Claves en las que un administrador puede escribir. (Si un administrador no puede escribir en una clave, la aplicación habría producido un error en las versiones anteriores de Windows, incluso si la ejecutara un administrador).

La virtualización del registro está deshabilitada para lo siguiente:

-   procesos de 64 bits.
-   Procesos que no son interactivos, como servicios.

    Tenga en cuenta que el uso del registro como un mecanismo de comunicación entre procesos (IPC) entre un servicio (o cualquier otro proceso que no tenga la virtualización habilitada) y una aplicación no funcionarán correctamente si la clave está virtualizada. Por ejemplo, si un servicio antivirus actualiza sus archivos de firma en función de un valor establecido por una aplicación, el servicio nunca actualizará sus archivos de firma porque el servicio Lee del almacén global pero la aplicación escribe en el almacén virtual.

-   Procesos que suplantan a un usuario. Si un proceso intenta una operación durante la suplantación de un usuario, esa operación no se virtualizará.
-   Procesos de modo kernel, como los controladores.
-   Procesos que tienen **requestedExecutionLevel** especificado en sus manifiestos.
-   Claves y subclaves **de \_ \_ \\ \\ las clases de software de máquina local HKEY**, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows** y **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Controlar la virtualización del registro

Además de controlar la virtualización en un nivel de aplicación mediante **requestedExecutionLevel** en el manifiesto, un administrador puede habilitar o deshabilitar la virtualización por clave para las claves en el **\_ software del \_ equipo \\ local HKEY**. Para ello, use la Reg.exe opción de marcas de la utilidad de línea de comandos con las marcas que aparecen en la tabla siguiente.



| Marca                         | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| error de la clave de registro \_ \_ \_ no silenciosa \_ | Esta marca deshabilita la virtualización del registro abierta. Si se establece esta marca y se produce un error en una operación de apertura en una clave que tiene habilitada la virtualización, el registro no intenta volver a abrir la clave. Si esta marca está desactivada, el registro intenta volver a abrir la clave con el \_ acceso máximo permitido en lugar del acceso solicitado.                                                                   |
| clave de registro no \_ \_ \_ virtualizar   | Esta marca deshabilita la virtualización del registro de escritura. Si se establece esta marca y se produce un error en una operación de creación de clave o valor, porque el autor de la llamada no tiene suficientes derechos de acceso a la clave primaria, el registro produce un error en la operación. Si esta marca está desactivada, el registro intenta escribir la clave o el valor en el almacén virtual. El autor de la llamada debe tener el \_ derecho de lectura de la clave en la clave primaria. |
| \_marca de \_ recursividad de clave de registro \_      | Si se establece esta marca, las marcas de virtualización del registro se propagan desde la clave primaria. Si esta marca está desactivada, las marcas de virtualización del registro no se propagan. El cambio de esta marca afecta solo a las nuevas claves descendientes creadas después de cambiar la marca. No establece ni borra estas marcas para las claves descendientes existentes.                                                                  |



 

En el ejemplo siguiente se muestra el uso de la utilidad de línea de comandos Reg.exe con la opción FLAGs para consultar el estado de las marcas de virtualización de una clave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Cada vez que se habilita la auditoría en una clave que se está virtualizando, se genera un nuevo evento de auditoría de virtualización para indicar que la clave se está virtualizando (además de los eventos de auditoría habituales). Los administradores pueden usar esta información para supervisar el estado de la virtualización en sus sistemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con control de cuentas de usuario](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Descripción y configuración del control de cuentas de usuario](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Prácticas recomendadas para desarrolladores e instrucciones para aplicaciones en un entorno con privilegios mínimos](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
