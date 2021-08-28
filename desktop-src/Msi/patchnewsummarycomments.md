---
description: La propiedad PATCHNEWSUMMARYCOMMENTS actualiza la propiedad Resumen de comentarios de una instalación administrativa durante la aplicación de revisiones.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: PatchNEWSUMMARYCOMMENTS, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074785"
---
# <a name="patchnewsummarycomments-property"></a>PatchNEWSUMMARYCOMMENTS, propiedad

La **propiedad PATCHNEWSUMMARYCOMMENTS** actualiza la [**propiedad Resumen de**](comments-summary.md) comentarios de una instalación administrativa durante la aplicación de revisiones. Esta propiedad solo se establece mediante una transformación en un archivo .msp. El archivo .msp debe incluir una transformación que agrega esta propiedad a la [tabla Property y](property-table.md) establece su valor. A continuación, el instalador escribe el valor **de PATCHNEWSUMMARYCOMMENTS en** la [**propiedad Resumen del número de revisión.**](revision-number-summary.md)

## <a name="remarks"></a>Comentarios

Las [**propiedades PATCHNEWPACKAGECODE,**](patchnewpackagecode.md) **PATCHNEWSUMMARYCOMMENTS** y [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) se usan para actualizar la información de resumen cuando se instala una revisión en una imagen administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




