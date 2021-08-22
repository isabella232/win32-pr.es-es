---
description: La propiedad PATCHNEWSUMMARYSUBJECT actualiza la propiedad Resumen del asunto de una imagen administrativa durante la aplicación de revisiones.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: PatchNEWSUMMARYSUBJECT, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926175"
---
# <a name="patchnewsummarysubject-property"></a>PatchNEWSUMMARYSUBJECT, propiedad

La **propiedad PATCHNEWSUMMARYSUBJECT** actualiza la [**propiedad Resumen del asunto**](subject-summary.md) de una imagen administrativa durante la aplicación de revisiones. Esta propiedad solo se establece mediante una transformación en un archivo .msp. El archivo .msp debe incluir una transformación que agrega esta propiedad a la [tabla Property y](property-table.md) establece su valor. A continuación, el instalador escribe el valor **de PATCHNEWSUMMARYSUBJECT en** la [**propiedad Resumen del número de**](revision-number-summary.md) revisión.

## <a name="remarks"></a>Comentarios

Las [**propiedades PATCHNEWPACKAGECODE,**](patchnewpackagecode.md) [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)y **PATCHNEWSUMMARYSUBJECT** se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




