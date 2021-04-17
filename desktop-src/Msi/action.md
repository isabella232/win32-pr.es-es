---
description: La propiedad ACTION se puede establecer en los valores siguientes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653762"
---
# <a name="action-property"></a>ACTION (propiedad)

La propiedad **Action** se puede establecer en los valores siguientes.

## <a name="value"></a>Value



| Value                                                                                                                                            | Significado                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**INSTALADOS**</dt> </dl>       | [Acción de instalación](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**ANUNCIA**</dt> </dl> | [Acción de anuncio](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ADMINISTRAR**</dt> </dl>             | [Acción de administración](admin-action.md)<br/>         |



 

La propiedad **Action** determina la acción que se realizará si se proporciona un nombre de acción null a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al [**método OnAction**](session-doaction.md). Si no se define ningún valor para la propiedad **Action** , el instalador llama a la [acción de instalación](install-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




