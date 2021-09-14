---
description: Si se establece la propiedad LIMITUI, el nivel de interfaz de usuario (UI) usado al instalar el paquete se restringe a Básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propiedad LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071964"
---
# <a name="limitui-property"></a>Propiedad LIMITUI

Si se **establece la propiedad LIMITUI,** el nivel de interfaz de usuario (UI) usado al instalar el paquete se restringe a Básico. Esta propiedad es necesaria en paquetes que no tienen ninguna interfaz de usuario de creación pero que todavía contienen tablas de interfaz de usuario como la [tabla Dialog](dialog-table.md). Para obtener una descripción de los niveles de interfaz de usuario, [ **vea MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Observaciones

Los paquetes de instalación que **contienen la propiedad LIMITUI** también deben contener [**la propiedad ARPNOMODIFY.**](arpnomodify.md) Esto es necesario para que un usuario  obtenga el comportamiento correcto de agregar o quitar programas en la utilidad **Panel de control** al intentar configurar un producto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




