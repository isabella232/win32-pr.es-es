---
description: Si se establece la propiedad LIMITUI, el nivel de interfaz de usuario (UI) usado al instalar el paquete se restringe a Básico.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: LimitUI, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013143"
---
# <a name="limitui-property"></a>LimitUI, propiedad

Si se establece la propiedad **LIMITUI,** el nivel de interfaz de usuario (UI) usado al instalar el paquete se restringe a Básico. Esta propiedad es necesaria en paquetes que no tienen ninguna interfaz de usuario de creación pero que todavía contienen tablas de interfaz de usuario como la [tabla Dialog](dialog-table.md). Para obtener una descripción de los niveles de interfaz de usuario, [ **vea MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Comentarios

Los paquetes de instalación que **contienen la propiedad LIMITUI** también deben contener [**la propiedad ARPNOMODIFY.**](arpnomodify.md) Esto es necesario para que un usuario  obtenga el comportamiento correcto de agregar o quitar programas en la utilidad **Panel de control** al intentar configurar un producto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




