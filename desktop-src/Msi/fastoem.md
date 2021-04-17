---
description: La propiedad FASTOEM está diseñada para permitir a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones para un escenario específico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: propiedad FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690988"
---
# <a name="fastoem-property"></a>propiedad FASTOEM

La propiedad **FASTOEM** está diseñada para permitir a los OEM reducir el tiempo necesario para instalar Windows Installer aplicaciones para un escenario específico. No cree la propiedad **FASTOEM** en la [tabla de propiedades](property-table.md).

La propiedad **FASTOEM** solo es aplicable si se cumplen todas estas condiciones:

-   La aplicación se está instalando en el mismo volumen que la carpeta que contiene los archivos de origen.
-   Los archivos de origen se eliminan después de la instalación.
-   No se muestra ninguna interfaz de usuario durante la instalación. El [nivel](user-interface-levels.md) de la interfaz de usuario es None.
-   La instalación se realiza en el [contexto de instalación](installation-context.md)por máquina.
-   Hay suficiente espacio en el equipo para una instalación correcta.
-   Esta es la primera vez que se instala. La instalación no está anunciando, reinstalando, quitando o realizando una instalación administrativa.
-   No hay características instaladas para ejecutarse desde el origen.
-   El paquete de instalación no contiene ningún [componente aislado](isolated-components.md). Dado que los componentes aislados requieren que los archivos de código fuente permanezcan ubicados en el origen, la propiedad **FASTOEM** no se puede usar actualmente con componentes aislados.

Si se cumplen todas las condiciones anteriores, el establecimiento de la propiedad **FASTOEM** permite a Windows Installer mejorar el rendimiento haciendo lo siguiente:

-   Mueva en lugar de copiar archivos en el mismo volumen. Esto no garantiza que todos los archivos se muevan en lugar de copiarse. Tenga en cuenta que si el equipo tiene varias unidades de disco duro, debe inicializar la propiedad [**ROOTDRIVE**](rootdrive.md) en la línea de comandos en la misma unidad que contiene el origen de instalación.
-   Omita este origen de la lista de origen de la aplicación para que las instalaciones de reinstalación o mantenimiento posteriores tengan como valor predeterminado los orígenes de CD-ROM especificados en la [tabla de medios](media-table.md).
-   Optimice el costo de los [archivos](file-costing.md).
-   Suprime los mensajes de progreso enviados desde Windows Installer al cliente.

## <a name="remarks"></a>Observaciones

Dado que no se envía ningún mensaje de progreso cuando se establece **FASTOEM** , se recomienda que los autores escriban manualmente un valor de 1800 para el tiempo de espera en la clave.

**HKLM** \\ **Software** \\ de **Directivas** \\ de **Microsoft** \\ **Windows** \\ **Instalador** \\ de **Tiempo de espera**

Timeout es un tipo de **Registro \_ DWORD** .

Para mostrar el tamaño de la aplicación en Agregar o quitar programas en el panel de control de Windows 2000, debe escribir manualmente el valor de EstimatedSize en la clave.

**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **<  Código > de producto**

Se trata de un tipo de **Registro \_ DWORD** y es igual al tamaño de la aplicación en Kbytes. El instalador no escribe este valor automáticamente.

Utilice la siguiente línea de comandos de ejemplo si el CD-ROM enviado a los usuarios finales almacena el paquete de instalación de la aplicación en la raíz del CD-ROM. Tenga en cuenta que la etiqueta de volumen de la [tabla de medios](media-table.md) del archivo. msi debe coincidir con la etiqueta de volumen del CD-ROM.

**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**

Utilice la siguiente línea de comandos de ejemplo si el paquete de instalación no se encuentra en la raíz del CD-ROM enviado a los usuarios finales. Debe establecer la propiedad [**MEDIAPACKAGEPATH**](mediapackagepath.md) en este caso en la ruta de acceso al paquete de instalación. La etiqueta de volumen de la [tabla de medios](media-table.md) del archivo. msi debe coincidir con la etiqueta de volumen del CD-ROM. En este caso, siga este ejemplo.

**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = C: \\ TempImage \\package.msi ROOTDRIVE = c:\\**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




