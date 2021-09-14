---
description: La propiedad FASTOEM está diseñada para permitir que los OEM reduzcan el tiempo necesario para instalar Windows Installer para un escenario específico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: propiedad FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158414"
---
# <a name="fastoem-property"></a>propiedad FASTOEM

La **propiedad FASTOEM** está diseñada para permitir que los OEM reduzcan el tiempo necesario para instalar Windows Installer para un escenario específico. No cree la **propiedad FASTOEM** en la [tabla de propiedades](property-table.md).

La **propiedad FASTOEM** solo es aplicable si se cumplen todas estas condiciones:

-   La aplicación se instala en el mismo volumen que la carpeta que contiene los archivos de origen.
-   Los archivos de origen se eliminan después de la instalación.
-   No se muestra ninguna interfaz de usuario durante la instalación. El [nivel de interfaz de usuario](user-interface-levels.md) no es ninguno.
-   La instalación se realiza en el contexto de instalación [por máquina](installation-context.md).
-   Hay suficiente espacio en el equipo para una instalación correcta.
-   Es la primera vez que se instala. La instalación no anuncia, reinstala, quita o hace una instalación administrativa.
-   No se instala ninguna características para ejecutarse desde el origen.
-   El paquete de instalación no contiene [componentes aislados.](isolated-components.md) Dado que los componentes aislados requieren que los archivos de origen permanezcan ubicados en el origen, la propiedad **FASTOEM** no se puede usar actualmente con componentes aislados.

Si se cumplen todas las condiciones anteriores, el establecimiento de la propiedad **FASTOEM** permite que Windows Installer mejore el rendimiento haciendo lo siguiente:

-   Mover en lugar de copiar archivos en el mismo volumen. Esto no garantiza que todos los archivos se mueven en lugar de copiarse. Tenga en cuenta que si el equipo tiene varias unidades de disco duro, debe inicializar la propiedad [**ROOTDRIVE**](rootdrive.md) en la línea de comandos en la misma unidad que contiene el origen de instalación.
-   Omita este origen de la lista de origen de la aplicación para que las instalaciones de reinstalación o mantenimiento posteriores se ajusten de forma predeterminada a los orígenes de CD-ROM especificados en [la tabla multimedia](media-table.md).
-   [Optimice el costo de archivos.](file-costing.md)
-   Suprima los mensajes de progreso enviados Windows instalador al cliente.

## <a name="remarks"></a>Observaciones

Dado que no se envía ningún mensaje de progreso cuando se establece **FASTOEM,** se recomienda que los autores escriban manualmente un valor de 1800 para Tiempo de espera en la clave.

**HKLM** \\ **SoftWare** \\ **Directivas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **Tiempo de espera**

Timeout es un **tipo \_ REG DWORD.**

Para mostrar el tamaño de la aplicación en Agregar o quitar programas en Windows 2000 Panel de control, debe escribir manualmente el valor de EstimatedSize en la clave.

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalación** \\ **< *Código de producto* >**

Se trata de **un \_ tipo REG DWORD** y es igual al tamaño de la aplicación en Kbytes. El instalador no escribe automáticamente este valor.

Use la siguiente línea de comandos de ejemplo si el CD-ROM enviado a los usuarios finales almacena el paquete de instalación de la aplicación en la raíz del CD-ROM. Tenga en cuenta que la etiqueta de volumen de [la](media-table.md) tabla multimedia del archivo .msi debe coincidir con la etiqueta de volumen del CD-ROM.

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**

Use la siguiente línea de comandos de ejemplo si el paquete de instalación no se encuentra en la raíz del CD-ROM enviado a los usuarios finales. En este caso, debe [**establecer la propiedad MEDIAPACKAGEPATH**](mediapackagepath.md) en la ruta de acceso al paquete de instalación. La etiqueta de volumen de [la tabla](media-table.md) multimedia del archivo .msi debe coincidir con la etiqueta de volumen del CD-ROM. En este caso, siga este ejemplo.

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C: \\ TempImage \\package.msi ROOTDRIVE=C:\\**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




