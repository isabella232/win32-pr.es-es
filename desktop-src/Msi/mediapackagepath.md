---
description: 'Si el paquete de instalación que se envía con una aplicación no se encuentra en la raíz del CD-ROM que reciben los clientes, la propiedad MEDIAPACKAGEPATH debe establecerse en la línea de comandos para la ruta de acceso relativa de la aplicación en el CD-ROM. Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ mypath \\My.msi, use MEDIAPACKAGEPATH =&\# 0034; \\ MyPath \\ & \# 0034;. Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa. Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad MEDIAPACKAGEPATH debe establecerse en la nueva ruta de acceso que se va a instalar desde este medio. No se puede usar un origen con una ubicación en el CD-ROM diferente de la especificada en el paquete. Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde los medios de envío.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propiedad MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680490"
---
# <a name="mediapackagepath-property"></a>Propiedad MEDIAPACKAGEPATH

Si el paquete de instalación que se envía con una aplicación no se encuentra en la raíz del CD-ROM que reciben los clientes, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la línea de comandos para la ruta de acceso relativa de la aplicación en el CD-ROM.

Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ mypath \\My.msi, use MEDIAPACKAGEPATH = " \\ myPath \\ ".

Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa. Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la nueva ruta de acceso que se va a instalar desde este medio. No se puede usar un origen con una ubicación en el CD-ROM diferente de la especificada en el paquete. Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde los medios de envío.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




