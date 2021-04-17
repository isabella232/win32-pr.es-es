---
description: La propiedad UPGRADINGPRODUCTCODE se establece mediante Windows Installer cuando una actualización quita una aplicación.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propiedad UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653629"
---
# <a name="upgradingproductcode-property"></a>Propiedad UPGRADINGPRODUCTCODE

La propiedad **UPGRADINGPRODUCTCODE** se establece mediante Windows Installer cuando una actualización quita una aplicación. El instalador establece esta propiedad cuando ejecuta la [acción RemoveExistingProducts](removeexistingproducts-action.md). Esta propiedad no se establece quitando una aplicación mediante agregar o quitar programas en el panel de control. Una aplicación determina si se va a quitar mediante una actualización o agregar o quitar programas comprobando **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




