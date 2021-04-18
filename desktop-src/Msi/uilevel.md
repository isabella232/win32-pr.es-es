---
description: El instalador establece la propiedad elemento uilevel en el nivel de la interfaz de usuario.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propiedad elemento uilevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679557"
---
# <a name="uilevel-property"></a>Propiedad elemento uilevel

El instalador establece la propiedad **elemento uilevel** en el nivel de la interfaz de usuario. La interfaz de usuario interna está habilitada y establecida por [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLUILEVEL.



| INSTALLUILEVEL          | Valor numérico | Nivel de interfaz de usuario                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ ninguno    | 2             | Instalación totalmente silenciosa.             |
| INSTALLUILEVEL \_ básico   | 3             | Progreso simple y control de errores.         |
| INSTALLUILEVEL \_ reducido | 4             | Interfaz de usuario creada, se han suprimido los cuadros de diálogo del asistente.     |
| INSTALLUILEVEL \_ completo    | 5             | Interfaz de usuario creada con asistentes, progreso y errores. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Interfaz de usuario](user-interface.md)
</dt> <dt>

[Determinar el nivel de interfaz de usuario a partir de una acción personalizada](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




