---
description: 'Si el envío del paquete de instalación con una aplicación no está en la raíz del CD-ROM que reciben los clientes, la propiedad MEDIAPACKAGEPATH debe establecerse en la línea de comandos a la ruta de acceso relativa de la aplicación en el CD-ROM. Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ MyPathMy.msi, use \\ MEDIAPACKAGEPATH=&\# 0034; \\ MyPath \\ & \# 0034;. Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa. Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad MEDIAPACKAGEPATH debe establecerse en la nueva ruta de acceso para instalar desde este medio. Un origen con una ubicación en el CD-ROM diferente de lo que se especifica en el paquete no es utilizable. Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde medios de envío.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propiedad MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074401"
---
# <a name="mediapackagepath-property"></a>Propiedad MEDIAPACKAGEPATH

Si el envío del paquete de instalación con una aplicación no está en la raíz del CD-ROM que reciben los clientes, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la línea de comandos a la ruta de acceso relativa de la aplicación en el CD-ROM.

Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ MyPath \\My.msi, use MEDIAPACKAGEPATH=" \\ MyPath \\ ".

Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa. Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la nueva ruta de acceso para instalar desde este medio. Un origen con una ubicación en el CD-ROM diferente de lo que se especifica en el paquete no es utilizable. Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde medios de envío.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




