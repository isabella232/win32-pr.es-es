---
description: La propiedad MsiHiddenProperties se puede usar para evitar que el instalador muestre contraseñas u otra información confidencial en el archivo de registro.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propiedad MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071849"
---
# <a name="msihiddenproperties-property"></a>Propiedad MsiHiddenProperties

La **propiedad MsiHiddenProperties** se puede usar para evitar que el instalador muestre contraseñas u otra información confidencial en el archivo de registro. Para evitar que una propiedad se escriba en el archivo de registro, establezca el valor de la propiedad **MsiHiddenProperties** en el nombre de la propiedad que desea ocultar. Puede ocultar varias propiedades especificando una cadena de nombres de propiedad delimitados por punto y coma (;).

> [!Note]  
> Cuando la [directiva de](debug.md) depuración se establece en un valor de 7, el instalador escribirá la información especificada en una línea de comandos en el registro. Esto hace que las propiedades públicas especificadas en una línea de comandos sean visibles incluso si la propiedad está incluida en **la propiedad MsiHiddenProperties.** Esto puede hacer que la información confidencial especificada en una línea de comandos sea visible en el registro. Para obtener más información, vea [Evitar que la información confidencial se escriba en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




