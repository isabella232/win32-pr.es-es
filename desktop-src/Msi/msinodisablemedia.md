---
description: Establezca la propiedad MSINODISABLEMEDIA para evitar que el instalador establezca la propiedad DISABLEMEDIA. Establecer la propiedad DISABLEMEDIA impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propiedad MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd4179995de7d509699b642ea7314497206d300850c3a83915dcdbd9901d2a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082845"
---
# <a name="msinodisablemedia-property"></a>Propiedad MSINODISABLEMEDIA

Establezca la **propiedad MSINODISABLEMEDIA para** evitar que el instalador establezca [**la propiedad DISABLEMEDIA.**](-disablemedia.md) Establecer la **propiedad DISABLEMEDIA** impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto.

Si **no se establece MSINODISABLEMEDIA,** el instalador podría agregar [**DISABLEMEDIA**](-disablemedia.md) al flujo de propiedades administrativas al realizar [una instalación administrativa.](administrative-installation.md) Esto evita que los usuarios que instalan desde la imagen administrativa se instalen desde medios, como un CD-ROM.

-   Al realizar una instalación administrativa, el instalador solo agrega [](page-count-summary.md) [**DISABLEMEDIA**](-disablemedia.md) al flujo de propiedades administrativas si la propiedad Resumen de recuento de páginas es inferior a 150.

Si [**DISABLEMEDIA aparece**](-disablemedia.md) en la [**propiedad AdminProperties,**](adminproperties.md) al establecer **MSINODISABLEMEDIA** se evita que **DISABLEMEDIA** se establezca durante una instalación administrativa. En este caso, el instalador puede registrar un origen multimedia y un usuario podría tener la opción de volver a instalarlo desde el origen de medios si la imagen de instalación administrativa original no estaba disponible más adelante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003, Windows XP y Windows 2000. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




