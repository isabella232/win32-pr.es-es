---
description: Si se establece la propiedad LIMITUI, el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propiedad LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690042"
---
# <a name="limitui-property"></a>Propiedad LIMITUI

Si se establece la propiedad **LIMITUI** , el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico. Esta propiedad es necesaria en los paquetes que no tienen ninguna interfaz de usuario creada pero que todavía contienen tablas de interfaz de usuario como la [tabla de diálogo](dialog-table.md). Para obtener una descripción de los niveles de interfaz de usuario, consulte [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Observaciones

Los paquetes de instalación que contienen la propiedad **LIMITUI** también deben contener la propiedad [**ARPNOMODIFY**](arpnomodify.md) . Esto es necesario para que un usuario obtenga el comportamiento correcto de **Agregar o quitar programas** en la utilidad del **Panel de control** al intentar configurar un producto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




