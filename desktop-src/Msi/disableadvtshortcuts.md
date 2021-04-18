---
description: Al establecer la propiedad DISABLEADVTSHORTCUTS, se deshabilita la generación de accesos directos que admiten la instalación a petición y el anuncio. Al establecer esta propiedad, se especifica que estos métodos abreviados se deben reemplazar por métodos abreviados normales.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propiedad DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653309"
---
# <a name="disableadvtshortcuts-property"></a>Propiedad DISABLEADVTSHORTCUTS

Al establecer la propiedad **DISABLEADVTSHORTCUTS** , se deshabilita la generación de accesos directos que admiten la [instalación a petición](installation-on-demand.md) y el [anuncio](advertisement.md). Al establecer esta propiedad, se especifica que estos métodos abreviados se deben reemplazar por métodos abreviados normales.

## <a name="default-value"></a>Valor predeterminado

De forma predeterminada, la generación de accesos directos de instalación a petición está habilitada.

## <a name="remarks"></a>Observaciones

Los métodos abreviados que admiten el anuncio tienen el nombre de una característica, en lugar de una ruta de acceso de archivo con formato con el formato \[ \# filekey, que se \] escribe en la columna de destino de la [tabla de acceso directo](shortcut-table.md). Si se establece esta propiedad y se instala la característica, el instalador genera un acceso directo normal a la característica.

Los administradores suelen usar esta propiedad para los usuarios que se desplazan entre los entornos que no admiten publicidad. Esta propiedad se puede establecer mediante una transformación, en la secuencia administrativa o en la [tabla de propiedades](property-table.md). Si se establece mediante la línea de comandos o mediante una llamada a [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), se debe restablecer de nuevo durante cada instalación posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




