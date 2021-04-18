---
description: Establezca la propiedad MSIUSEREALADMINDETECTION en 1 para solicitar que el instalador use información de usuario real al establecer la propiedad AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propiedad MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680789"
---
# <a name="msiuserealadmindetection-property"></a>Propiedad MSIUSEREALADMINDETECTION

Establezca la propiedad **MSIUSEREALADMINDETECTION** en 1 para solicitar que el instalador use información de usuario real al establecer la propiedad [**AdminUser**](adminuser.md) . Cuando se ejecuta en Windows Vista, [**privileged**](privileged.md) y **AdminUser** son los mismos. Los autores deben usar la propiedad **privileged** en los nuevos paquetes. Los paquetes heredados que requieren distintas propiedades **privileged** y **AdminUser** pueden restaurar la diferencia estableciendo la propiedad **MSIUSEREALADMINDETECTION** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




