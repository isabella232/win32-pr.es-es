---
description: La propiedad MSIARPSETTINGSIDENTIFIER contiene una lista delimitada por punto y coma de las ubicaciones del Registro donde la aplicación almacena la configuración y las preferencias de un usuario.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propiedad MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261076"
---
# <a name="msiarpsettingsidentifier-property"></a>Propiedad MSIARPSETTINGSIDENTIFIER

La **propiedad MSIARPSETTINGSIDENTIFIER** contiene una lista delimitada por punto y coma de las ubicaciones del Registro donde la aplicación almacena la configuración y las preferencias de un usuario. Durante una actualización del sistema operativo, el programa de instalación puede usar esta información para mejorar la experiencia de los usuarios que migran aplicaciones.

El valor de la **propiedad MSIARPSETTINGSIDENTIFIER** es texto literal que contiene la lista de ubicaciones del Registro donde la aplicación almacena su configuración. El valor puede especificar varias ubicaciones de registro posibles. Separe varias ubicaciones del Registro mediante punto y coma. La configuración de la aplicación se almacena normalmente en los subárboles del Registro **HKCU** **o HKLM** con el formato: *Versión de la aplicación \\ de \\ empresa*. El ejemplo siguiente es un valor posible para **la propiedad MSIARPSETTINGSIDENTIFIER.**

*MyCompany \\ AppSuite \\ 1.0; MyCompany \\ App1 \\ 1.0; MyCompany \\ App2 \\ 1.0*

Esta propiedad es opcional y se puede establecer en la [tabla Property.](property-table.md) Si esta propiedad aparece en la tabla Property, el valor no debe establecerse en **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




