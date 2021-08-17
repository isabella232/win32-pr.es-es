---
description: Esta Windows installer indica cuándo se ha establecido el nivel de interfaz de usuario interno para ocultar el botón Cancelar.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propiedad MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da3c0888ea760e7e8627710b061112d350f94af569697b7ad0616d1dbacbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943993"
---
# <a name="msiuihidecancel-property"></a>Propiedad MsiUIHideCancel

El instalador establece la propiedad **MsiUIHideCancel** en 1 cuando se ha establecido el nivel de interfaz de usuario interno para incluir INSTALLUILEVEL HIDECANCEL con la función \_ [](command-line-options.md) [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la propiedad [UILevel](installer-uilevel.md)del objeto [**Installer**](installer-object.md) o mediante opciones de línea de comandos .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




