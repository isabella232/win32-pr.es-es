---
description: La propiedad ACTION se puede establecer en los valores siguientes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Action, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159236"
---
# <a name="action-property"></a>Action, propiedad

La **propiedad ACTION** se puede establecer en los valores siguientes.

## <a name="value"></a>Value



| Value                                                                                                                                            | Significado                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**INSTALAR**</dt> </dl>       | [Acción INSTALL](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**ANUNCIAR**</dt> </dl> | [Acción ADVERTISE](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ADMIN**</dt> </dl>             | [Acción admin](admin-action.md)<br/>         |



 

La **propiedad ACTION** determina qué acción realizar si se proporciona un nombre de acción NULL a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al método [**DoAction**](session-doaction.md). Si no se define ningún valor para la **propiedad ACTION,** el instalador llama a [la acción INSTALL](install-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




