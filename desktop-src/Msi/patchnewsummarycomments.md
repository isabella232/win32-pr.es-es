---
description: La propiedad PATCHNEWSUMMARYCOMMENTS actualiza la propiedad de Resumen comentarios de una instalación administrativa durante la revisión.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Propiedad PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653414"
---
# <a name="patchnewsummarycomments-property"></a>Propiedad PATCHNEWSUMMARYCOMMENTS

La propiedad **PATCHNEWSUMMARYCOMMENTS** actualiza la propiedad de [**Resumen comentarios**](comments-summary.md) de una instalación administrativa durante la revisión. Esta propiedad solo se establece mediante una transformación en un archivo. msp. El archivo. MSP debe incluir una transformación que agregue esta propiedad a la [tabla de propiedades](property-table.md) y establezca su valor. Después, el instalador escribe el valor de **PATCHNEWSUMMARYCOMMENTS** en la propiedad [**Summary del número de revisión**](revision-number-summary.md) .

## <a name="remarks"></a>Observaciones

Las propiedades [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




