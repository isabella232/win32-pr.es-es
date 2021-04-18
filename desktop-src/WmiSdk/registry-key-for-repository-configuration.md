---
description: Instrumental de administración de Windows (WMI) tiene una nueva clave del registro para habilitar o deshabilitar la característica de repositorio de restauración.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Clave del registro para la configuración del repositorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706096"
---
# <a name="registry-key-for-repository-configuration"></a>Clave del registro para la configuración del repositorio

Instrumental de administración de Windows (WMI) tiene una nueva clave del registro para habilitar o deshabilitar la característica de repositorio de restauración. Para obtener más información acerca de la restauración del repositorio WMI, vea [copia de seguridad o restauración del repositorio WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

En Windows 7, el comportamiento predeterminado es la restauración automática de un repositorio a partir de una versión de copia de seguridad si se detecta un daño en el repositorio. WMI proporciona el valor del registro **AutoRestoreEnabled** para deshabilitar esta característica.

Las claves del registro para WMI se encuentran en el registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Permite al usuario determinar si se usa o no la característica de repositorio de restauración. De forma predeterminada, esta clave se establece en 1 y está habilitada la característica de repositorio de restauración.

Las siguientes opciones son posibles:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

habilitado

</dd> </dl> </dd> </dl>

El valor del registro **AutoRestoreEnabled** se puede modificar mediante el consola de administración de directivas de grupo (GPMC). Para obtener más información, vea [consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

En este procedimiento se proporcionan detalles acerca de cómo habilitar o deshabilitar la característica de repositorio de restauración.

**Para cambiar el valor predeterminado de la clave **AutoRestoreEnabled** mediante Directiva de grupo**

1.  Abra GPMC.
2.  Cree un objeto de directiva de grupo (GPO).
3.  Edite el GPO.
4.  Vaya a preferencias/configuración de Windows/registro.
5.  Haga clic con el botón derecho y seleccione **nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.
6.  Seleccione el comando de **actualización** .
7.  Seleccione la siguiente ruta de acceso de clave del registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.
8.  En el campo **nombre** , escriba **AutoRestoreEnabled**.
9.  En el campo de **datos** , escriba 0 para deshabilitar o 1 para habilitar la característica de repositorio de restauración.
10. Haga clic en Aceptar.

 

 
