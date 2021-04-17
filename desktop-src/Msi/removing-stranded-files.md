---
description: Una lista de posibles razones por las que un Windows Installer desinstalación no pudo quitar todos los archivos de una aplicación.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Quitar archivos en desuso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667669"
---
# <a name="removing-stranded-files"></a>Quitar archivos en desuso

Si un archivo que se debe haber quitado del equipo del usuario permanece instalado después de ejecutar una desinstalación, es posible que el instalador no esté quitando el componente que contiene el archivo por una o varias de las razones siguientes:

-   Se estableció el bit msidbComponentAttributesPermanent para el componente en la columna Attributes de la [tabla Component](component-table.md).
-   No se especificó ningún valor para el componente en la columna ComponentId de la tabla de componentes.
-   El componente lo usa otra aplicación o característica que todavía está instalada.
-   Existe una condición especificada en la tabla de [condiciones](condition-table.md) que habilita una característica durante la instalación y deshabilita la característica durante la desinstalación.
-   El archivo de clave del componente tiene un recuento de referencias anterior en **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   El componente se instala en la carpeta del sistema y cualquier archivo del componente tiene un recuento de referencias anterior en **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   El Windows Installer no quita los archivos ni las claves del registro que estén protegidos por [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) (WRP). Para obtener más información, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md). En Windows Server 2003, Windows XP y Windows 2000, el instalador no quita los archivos protegidos por protección de archivos de Windows (WFP). Si la clave del registro o el archivo de ruta de acceso de la clave de un componente están protegidos por WFP o WRP, el instalador no quita el componente.
    > [!Note]  
    > Dado que Windows Installer no instala, actualiza o quita ningún recurso que esté protegido por WRP, no debe incluir recursos protegidos en un paquete de instalación. En su lugar, use solo los [mecanismos de sustitución de recursos admitidos](../wfp/supported-file-replacement-mechanisms.md) que se describen en la sección [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) .

     

 

 
