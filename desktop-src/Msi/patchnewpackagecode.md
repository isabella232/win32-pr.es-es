---
description: La propiedad PATCHNEWPACKAGECODE actualiza la propiedad de resumen del número de revisión de una imagen administrativa durante la revisión.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propiedad PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670427"
---
# <a name="patchnewpackagecode-property"></a>Propiedad PATCHNEWPACKAGECODE

La propiedad **PATCHNEWPACKAGECODE** actualiza la propiedad de [**Resumen del número de revisión**](revision-number-summary.md) de una imagen administrativa durante la revisión. Esta propiedad solo se establece mediante una transformación en un archivo. msp. El archivo. MSP debe incluir una transformación que agregue esta propiedad a la [tabla de propiedades](property-table.md) y establezca su valor. Después, el instalador escribe el valor de **PATCHNEWPACKAGECODE** en la propiedad **Summary del número de revisión** .

## <a name="remarks"></a>Observaciones

Las propiedades **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




