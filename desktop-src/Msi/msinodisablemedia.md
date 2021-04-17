---
description: Establezca la propiedad MSINODISABLEMEDIA para evitar que el instalador establezca la propiedad DISABLEMEDIA. El establecimiento de la propiedad DISABLEMEDIA evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propiedad MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653784"
---
# <a name="msinodisablemedia-property"></a>Propiedad MSINODISABLEMEDIA

Establezca la propiedad **MSINODISABLEMEDIA** para evitar que el instalador establezca la propiedad [**DISABLEMEDIA**](-disablemedia.md) . El establecimiento de la propiedad **DISABLEMEDIA** evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.

Cuando no se establece **MSINODISABLEMEDIA** , el instalador puede agregar [**DISABLEMEDIA**](-disablemedia.md) al flujo de propiedades administrativas al realizar una [instalación administrativa](administrative-installation.md). Esto impide que los usuarios que se instalan desde la imagen administrativa se instalen desde un medio, como un CD-ROM.

-   Al realizar una instalación administrativa, el instalador solo agrega [**DISABLEMEDIA**](-disablemedia.md) a la secuencia de propiedades administrativas si la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es inferior a 150.

Si [**DISABLEMEDIA**](-disablemedia.md) aparece en la propiedad [**AdminProperties**](adminproperties.md) , al establecer **MSINODISABLEMEDIA** se impide que se establezca **DISABLEMEDIA** durante una instalación administrativa. En este caso, el instalador puede registrar un origen multimedia y un usuario podría tener la opción de reinstalar desde el origen de medios si la imagen de instalación administrativa original dejaba de estar disponible más adelante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003, Windows XP y Windows 2000. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




