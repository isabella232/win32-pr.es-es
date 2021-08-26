---
description: La propiedad PATCHNEWPACKAGECODE actualiza la propiedad Resumen del número de revisión de una imagen administrativa durante la aplicación de revisiones.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propiedad PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d7e64729643fa1b6449838496416d10e1ec12374762b3f702b306a146338f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926174"
---
# <a name="patchnewpackagecode-property"></a>Propiedad PATCHNEWPACKAGECODE

La **propiedad PATCHNEWPACKAGECODE** actualiza la propiedad Resumen del número [**de revisión**](revision-number-summary.md) de una imagen administrativa durante la aplicación de revisiones. Esta propiedad solo se establece mediante una transformación en un archivo .msp. El archivo .msp debe incluir una transformación que agrega esta propiedad a la [tabla Property y](property-table.md) establece su valor. A continuación, el instalador escribe el valor **de PATCHNEWPACKAGECODE en** la **propiedad Resumen del número de** revisión.

## <a name="remarks"></a>Comentarios

Las **propiedades PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




