---
description: Si un paquete de Windows Installer instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Claves del registro de ensamblado escritas por Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545182"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Claves del registro de ensamblado escritas por Windows Installer

Si un paquete de Windows Installer instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local. Tenga en cuenta que estas claves del registro solo están pensadas para que las use internamente Windows Installer y no deben depender de la aplicación. El contenido, la ubicación y la estructura de la información almacenada en estas claves están sujetos a cambios. Las aplicaciones deben basarse en [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para administrar ensamblados.

Los ensamblados se registran con los nombres de ensamblado. Los nombres de los valores almacenados en las siguientes ubicaciones son los nombres de ensamblado. Los valores reales son del tipo REG \_ multi \_ SZ y contienen datos usados por [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar o reparar ensamblados.

## <a name="information-about-private-assemblies"></a>Información sobre ensamblados privados

Windows Installer almacena información acerca de los ensamblados privados que llevan Windows Installer paquetes que se han instalado como aplicaciones administradas por usuario en la siguiente clave del registro:

**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ de **Administrados** \\ **SID *_\\_* de usuario Instalador** \\ de **ensamblados** \\ * *_ruta de acceso al archivo de configuración_* _

Windows Installer almacena información sobre los ensamblados privados que llevan Windows Installer paquetes que se han instalado por usuario en la siguiente clave del registro:

_*HKCU **\\** software **\\** Microsoft **\\** Installer **\\** ensamblados **\\** _ruta de acceso al archivo de configuración_*_

Windows Installer almacena información sobre los ensamblados privados que llevan Windows Installer paquetes y que se instalan por equipo en la siguiente clave del registro:

_*HKLM **\\** **\\** **\\** instalación de clases **\\** de software ensamblados **\\** _ruta de acceso al archivo de configuración_*_

## <a name="information-about-global-or-shared-assemblies"></a>Información sobre ensamblados globales o compartidos

Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes que se han instalado como aplicaciones administradas por usuario en la siguiente clave del registro:

_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User SID_*_ \\ _ *Installer **\\** assemblies **\\** global**

Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes que se han instalado por usuario en la siguiente clave del registro:

**HKCU** \\ **Software** \\ de **Microsoft** \\ **Instalador** \\ de **Ensamblados** \\ **Nivel global**

Windows Installer almacena información sobre los ensamblados compartidos que llevan Windows Installer paquetes y que se instalan por equipo en la siguiente clave del registro:

**HKLM** \\ **Software** \\ de **Clases** \\ de **Instalador** \\ de **Ensamblados** \\ **Nivel global**

 

 



