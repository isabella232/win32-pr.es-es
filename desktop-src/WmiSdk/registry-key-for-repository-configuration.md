---
description: Windows Instrumental de administración (WMI) tiene una nueva clave del Registro para habilitar o deshabilitar la característica de repositorio AutoRestore.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Clave del Registro para la configuración del repositorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973735"
---
# <a name="registry-key-for-repository-configuration"></a>Clave del Registro para la configuración del repositorio

Windows Instrumental de administración (WMI) tiene una nueva clave del Registro para habilitar o deshabilitar la característica de repositorio AutoRestore. Para obtener más información sobre cómo restaurar el repositorio WMI, vea [Copia de seguridad o restauración del repositorio WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

En Windows 7, el comportamiento predeterminado es restaurar automáticamente un repositorio desde una versión de copia de seguridad si se detectan daños en un repositorio. WMI proporciona el **valor del Registro AutoRestoreEnabled** para deshabilitar esta característica.

Las claves del Registro para WMI se encuentran en el registro en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Permite al usuario determinar si se debe usar o no la característica de repositorio AutoRestore. De forma predeterminada, esta clave se establece en 1 y la característica Repositorio de AutoRestore está habilitada.

La siguiente configuración es posible:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

habilitado

</dd> </dl> </dd> </dl>

El **valor del Registro AutoRestoreEnabled** se puede modificar mediante Consola de administración de directivas de grupo (GPMC). Para obtener más información, [vea Consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

En este procedimiento se proporcionan detalles sobre cómo habilitar o deshabilitar la característica de repositorio AutoRestore:

**Para cambiar el valor predeterminado de la **clave AutoRestoreEnabled** mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un directiva de grupo de datos (GPO).
3.  Edite el GPO.
4.  Vaya a Preferencias/Windows Configuración/Registro.
5.  Haga clic con el botón derecho y **seleccione Nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede escribir información del Registro.
6.  Seleccione el **comando** Actualizar.
7.  Seleccione la siguiente ruta de acceso de clave del Registro: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ WBEM \\ CIMOM**.
8.  En el **campo nombre,** escriba **AutoRestoreEnabled.**
9.  En el **campo de** datos, escriba 0 para deshabilitar o 1 para habilitar la característica de repositorio AutoRestore.
10. Haga clic en Aceptar.

 

 
