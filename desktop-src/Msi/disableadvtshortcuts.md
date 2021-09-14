---
description: Al establecer la propiedad DISABLEADVTSHORTCUTS, se deshabilita la generación de accesos directos que admiten la instalación a petición y el anuncio. Al establecer esta propiedad se especifica que estos accesos directos deben reemplazarse por métodos abreviados normales.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: DisableADVTSHORTCUTS, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158560"
---
# <a name="disableadvtshortcuts-property"></a>DisableADVTSHORTCUTS, propiedad

Al establecer **la propiedad DISABLEADVTSHORTCUTS,** se deshabilita la generación de accesos directos que admiten la instalación a [petición](advertisement.md) [y](installation-on-demand.md) el anuncio . Al establecer esta propiedad se especifica que estos accesos directos deben reemplazarse por métodos abreviados normales.

## <a name="default-value"></a>Valor predeterminado

De forma predeterminada, la generación de accesos directos a petición de instalación está habilitada.

## <a name="remarks"></a>Observaciones

Los accesos directos que admiten anuncios tienen el nombre de una característica, en lugar de una ruta de acceso de archivo con formato de la clave de archivo de formulario , especificada en la columna Destino de la tabla \[ \# \] Acceso [directo](shortcut-table.md). Si se establece esta propiedad y se instala la característica, el instalador genera un acceso directo normal a la característica.

Esta propiedad la usan normalmente los administradores para los usuarios que se desfilan entre entornos que sí admiten y no admiten publicidad. Esta propiedad se puede establecer mediante una transformación, en el flujo administrativo o en la [tabla Property](property-table.md). Si se establece mediante la línea de comandos o mediante una llamada a [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), se debe restablecer de nuevo durante cada instalación posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




