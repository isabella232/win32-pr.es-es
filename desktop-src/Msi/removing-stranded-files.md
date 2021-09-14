---
description: Lista de posibles motivos por los que Windows desinstalación del instalador no pudo quitar todos los archivos de una aplicación.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Eliminación de archivos desenlazados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274135"
---
# <a name="removing-stranded-files"></a>Eliminación de archivos desenlazados

Si un archivo que se debe haber quitado del equipo del usuario permanece instalado después de ejecutar una desinstalación, es posible que el instalador no quite el componente que contiene el archivo por uno o varios de los siguientes motivos:

-   El bit msidbComponentAttributesPermanent se estableció para el componente en la columna Atributos de la [tabla Component](component-table.md).
-   No se ha especificado ningún valor para el componente en la columna ComponentId de la tabla Component.
-   El componente lo usa otra aplicación o característica que todavía está instalada.
-   Hay una condición especificada en la tabla [Condición](condition-table.md) que habilita una característica durante la instalación y deshabilita la característica durante la desinstalación.
-   El archivo de clave del componente tiene un recuento de referencias anterior en **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\  \\ **SharedDLLs de** CurrentVersion .
-   El componente se instala en la carpeta System y cualquier archivo del componente tiene un recuento de referencias anterior en **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   El Windows no quita ningún archivo o clave del Registro protegido [por Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP). Para obtener más información, vea [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md). En Windows Server 2003, Windows XP y Windows 2000, el instalador no quita ningún archivo protegido por Windows File Protection (WFP). Si el archivo de ruta de acceso de clave o la clave del Registro de un componente está protegido por WFP o WRP, el instalador no quita el componente.
    > [!Note]  
    > Dado Windows instalador no instala, actualiza ni quita ningún recurso protegido por WRP, no debe incluir recursos protegidos en un paquete de instalación. En su lugar, use solo [los mecanismos de reemplazo de recursos admitidos que](../wfp/supported-file-replacement-mechanisms.md) se describen en la Windows Resource [Protection.](../wfp/windows-resource-protection-portal.md)

     

 

 
