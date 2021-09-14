---
description: La propiedad TARGETDIR especifica el directorio de destino raíz para la instalación.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propiedad TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069617"
---
# <a name="targetdir-property"></a>Propiedad TARGETDIR

La **propiedad TARGETDIR** especifica el directorio de destino raíz para la instalación. **TARGETDIR** debe ser el nombre de una raíz de la [tabla Directory.](directory-table.md) Puede haber solo un único directorio de destino raíz. Durante una [instalación administrativa,](administrative-installation.md) esta propiedad especifica la ubicación en la que se va a copiar el paquete de instalación. Durante una instalación no administrativa, esta propiedad especifica el directorio de destino raíz.

Para especificar el directorio de destino raíz, establezca la columna Directory de la tabla Directory en la propiedad **TARGETDIR** y la columna DefaultDir en la [**propiedad SourceDir.**](sourcedir.md) Si se define la propiedad **TARGETDIR,** el directorio de destino se resuelve en el valor de la propiedad. Si la **propiedad TARGETDIR** no está definida, se usa [**la propiedad ROOTDRIVE**](rootdrive.md) para resolver la ruta de acceso. Para obtener más información sobre el uso de **la propiedad TARGETDIR,** vea [Usar la tabla de directorios](using-the-directory-table.md).

Tenga en cuenta que el valor de la **propiedad TARGETDIR** se establece normalmente en la línea de comandos o a través de una interfaz de usuario. No **se recomienda establecer TARGETDIR** mediante la creación de una ruta de acceso en la tabla [Property](property-table.md) porque los equipos difieren en la configuración de la unidad local.

Para obtener más información sobre cómo cambiar TARGETDIR durante una instalación, vea [Cambiar la ubicación de destino de un directorio.](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




