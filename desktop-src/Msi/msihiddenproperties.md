---
description: La propiedad MsiHiddenProperties se puede usar para impedir que el instalador muestre contraseñas u otra información confidencial en el archivo de registro.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propiedad MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671049"
---
# <a name="msihiddenproperties-property"></a>Propiedad MsiHiddenProperties

La propiedad **MsiHiddenProperties** se puede usar para impedir que el instalador muestre contraseñas u otra información confidencial en el archivo de registro. Para evitar que una propiedad se escriba en el archivo de registro, establezca el valor de la propiedad **MsiHiddenProperties** en el nombre de la propiedad que desea ocultar. Puede ocultar varias propiedades si especifica una cadena de nombres de propiedad delimitados por punto y coma (;).

> [!Note]  
> Cuando la Directiva de [depuración](debug.md) está establecida en un valor de 7, el instalador escribe la información especificada en una línea de comandos en el registro. Esto hace que las propiedades públicas escritas en una línea de comandos sean visibles aunque la propiedad esté incluida en la propiedad **MsiHiddenProperties** . Esto puede hacer que la información confidencial especificada en una línea de comandos esté visible en el registro. Para obtener más información, vea [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




