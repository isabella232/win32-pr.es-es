---
description: El instalador establece la propiedad UPGRADINGPRODUCTCODE Windows cuando una actualización quita una aplicación.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propiedad UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f5b0096878d06c4eb3880ab8d965265b04114bcf4e3d732d8243bb4fb02cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809515"
---
# <a name="upgradingproductcode-property"></a>Propiedad UPGRADINGPRODUCTCODE

El instalador establece la propiedad **UPGRADINGPRODUCTCODE** Windows cuando una actualización quita una aplicación. El instalador establece esta propiedad cuando ejecuta la [acción RemoveExistingProducts](removeexistingproducts-action.md). Esta propiedad no se establece quitando una aplicación mediante agregar o quitar programas en Panel de control. Una aplicación determina si se va a quitar mediante una actualización o agregar o quitar programas mediante la comprobación **de UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




