---
description: Esta propiedad Windows Installer indica cuándo se ha establecido el nivel interno de la interfaz de usuario para ocultar el botón Cancelar.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propiedad MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680794"
---
# <a name="msiuihidecancel-property"></a>Propiedad MsiUIHideCancel

El instalador establece la propiedad **MsiUIHideCancel** en 1 cuando se ha establecido el nivel de la interfaz de usuario interna para incluir INSTALLUILEVEL \_ HIDECANCEL con la función [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la propiedad [elemento uilevel](installer-uilevel.md)del objeto [**Installer**](installer-object.md) o mediante opciones de la [línea de comandos](command-line-options.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




