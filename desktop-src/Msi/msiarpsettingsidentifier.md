---
description: La propiedad MSIARPSETTINGSIDENTIFIER contiene una lista delimitada por punto y coma de las ubicaciones del registro en las que la aplicación almacena las preferencias y la configuración de un usuario.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propiedad MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671414"
---
# <a name="msiarpsettingsidentifier-property"></a>Propiedad MSIARPSETTINGSIDENTIFIER

La propiedad **MSIARPSETTINGSIDENTIFIER** contiene una lista delimitada por punto y coma de las ubicaciones del registro en las que la aplicación almacena las preferencias y la configuración de un usuario. Durante una actualización del sistema operativo, el programa de instalación puede usar esta información para mejorar la experiencia de los usuarios que están migrando aplicaciones.

El valor de la propiedad **MSIARPSETTINGSIDENTIFIER** es un texto literal que contiene la lista de ubicaciones del registro donde la aplicación almacena su configuración. El valor puede especificar varias ubicaciones posibles del registro. Separe varias ubicaciones del registro mediante punto y coma. La configuración de la aplicación normalmente se almacena en los subárboles del registro **HKCU** o **HKLM** de la forma: *\\ \\ versión* de la aplicación de empresa. El ejemplo siguiente es un posible valor de la propiedad **MSIARPSETTINGSIDENTIFIER** .

*Mycompany \\ AppSuite \\ 1,0; Mycompany \\ App1 \\ 1,0; Mycompany \\ App2 \\ 1,0*

Esta propiedad es opcional y se puede establecer en la tabla de [propiedades](property-table.md) . Si esta propiedad aparece en la tabla de propiedades, el valor no debe establecerse en **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 4,5 en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




