---
description: La propiedad UPGRADINGPRODUCTCODE se establece mediante Windows instalador cuando una actualización quita una aplicación.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propiedad UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074288"
---
# <a name="upgradingproductcode-property"></a>Propiedad UPGRADINGPRODUCTCODE

La **propiedad UPGRADINGPRODUCTCODE** se establece mediante Windows instalador cuando una actualización quita una aplicación. El instalador establece esta propiedad cuando ejecuta la [acción RemoveExistingProducts](removeexistingproducts-action.md). Esta propiedad no se establece quitando una aplicación mediante agregar o quitar programas en Panel de control. Una aplicación determina si se va a quitar mediante una actualización o agregar o quitar programas mediante la comprobación **de UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




