---
description: Establezca la propiedad MSIUSEREALADMINDETECTION en 1 para solicitar que el instalador use información de usuario real al establecer la propiedad AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propiedad MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a177d320aff25cf21b932ca25e691f145f94ad3
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812938"
---
# <a name="msiuserealadmindetection-property"></a>Propiedad MSIUSEREALADMINDETECTION

Establezca la **propiedad MSIUSEREALADMINDETECTION** en 1 para solicitar que el instalador use información de usuario real al establecer la [**propiedad AdminUser.**](adminuser.md) Cuando se ejecuta Windows Vista, [**Privileged**](privileged.md) y **AdminUser** son los mismos. Los autores deben usar la **propiedad Privileged** en paquetes nuevos. Los paquetes heredados que requieren distintas propiedades **Privileged** **y AdminUser** pueden restaurar la diferencia estableciendo la **propiedad MSIUSEREALADMINDETECTION.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




