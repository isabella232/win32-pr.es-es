---
description: Establecer la propiedad DISABLEMEDIA impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: DisableMEDIA, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d56e6e50bdfe8a6ead05ad467caa355a7b6051715b65ec624e3cec6eea2affcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640460"
---
# <a name="disablemedia-property"></a>DisableMEDIA, propiedad

Establecer la [**propiedad DISABLEMEDIA**](disablemedia.md) impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que [**la propiedad DISABLEMEDIA**](disablemedia.md) tiene un efecto diferente al de establecer la directiva DisableMedia. Si **se establece DISABLEMEDIA,** se evita el registro de cualquier origen multimedia, lo que también impide la primera instalación de una aplicación desde un origen multimedia.

Para obtener más información sobre [](m-gly.md) cómo proteger los orígenes multimedia de la aplicación administrada contra la exploración y la instalación por parte de usuarios no [administrativos,](source-resiliency.md)vea Resistencia de origen .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




