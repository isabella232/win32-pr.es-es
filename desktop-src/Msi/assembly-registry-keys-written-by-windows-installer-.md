---
description: Si un Windows instalador instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Claves del Registro de ensamblado escritas por Windows Instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159065"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Claves del Registro de ensamblado escritas por Windows Instalador

Si un Windows instalador instala o anuncia ensamblados, el instalador almacena información sobre esos ensamblados en el registro del sistema local. Tenga en cuenta que estas claves del Registro solo están diseñadas para ser usadas internamente por Windows Installer y la aplicación no debe confiar en ellas. El contenido, la ubicación y la estructura de la información almacenada en estas claves están sujetos a cambios. Las aplicaciones deben basarse [**en MsiProvideAssembly para**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) administrar ensamblados.

Los ensamblados se registran por sus nombres de ensamblado. Los nombres de los valores almacenados en las siguientes ubicaciones son los nombres de ensamblado. Los valores reales son del tipo REG MULTI SZ y contienen datos usados por \_ \_ [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar o reparar ensamblados.

## <a name="information-about-private-assemblies"></a>Información sobre ensamblados privados

Windows El instalador almacena información sobre los ensamblados privados llevados por Windows Installer que se han instalado como aplicaciones administradas por usuario en la siguiente clave del Registro:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ **Administrado** \\ **_SID de usuario_ *_\\_* Ruta** \\ **de acceso de** \\ **_ensamblados del instalador al archivo de configuración_**

Windows El instalador almacena información sobre los ensamblados privados que Windows paquetes del instalador que se han instalado por usuario con la siguiente clave del Registro:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ **Ensamblados** \\ **_ruta de acceso al archivo de configuración_**

Windows El instalador almacena información sobre los ensamblados privados que Windows paquetes del instalador e instala por equipo con la siguiente clave del Registro:

**HKLM** \\ **SOFTWARE** \\ **Clases** \\ **Instalador** \\ **Ensamblados** \\ **_ruta de acceso al archivo de configuración_**

## <a name="information-about-global-or-shared-assemblies"></a>Información sobre ensamblados globales o compartidos

Windows El instalador almacena información sobre los ensamblados compartidos llevados por Windows Installer que se han instalado como aplicaciones administradas por usuario en la siguiente clave del Registro:

**HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ **Administrado** \\ **_SID de usuario_ *_\\_* Ensamblados** \\ **del instalador** \\ **globales**

Windows El instalador almacena información sobre los ensamblados compartidos llevados por Windows Installer que se han instalado por usuario con la siguiente clave del Registro:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ **Ensamblados** \\ **Global**

Windows El instalador almacena información sobre los ensamblados compartidos que Windows paquetes del instalador e instala por equipo con la siguiente clave del Registro:

**HKLM** \\ **SOFTWARE** \\ **Clases** \\ **Instalador** \\ **Ensamblados** \\ **Global**

 

 



