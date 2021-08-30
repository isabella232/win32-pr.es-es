---
description: El instalador establece la propiedad UILevel en el nivel de la interfaz de usuario.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: UiLevel, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73b9a3353e087abe882b45f0fdc41d13eeabff222266afd8e47100f22c8def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039404"
---
# <a name="uilevel-property"></a>UiLevel, propiedad

El instalador establece la **propiedad UILevel** en el nivel de la interfaz de usuario. [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)habilita y establece la interfaz de usuario interna. Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLUILEVEL.



| INSTALLUILEVEL          | Valor numérico | Nivel de interfaz de usuario                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ NONE    | 2             | Instalación totalmente silenciosa.             |
| INSTALLUILEVEL \_ BASIC   | 3             | Progreso sencillo y control de errores.         |
| INSTALLUILEVEL \_ REDUCIDO | 4             | Interfaz de usuario de creación, diálogos del asistente suprimidos.     |
| INSTALLUILEVEL \_ FULL    | 5             | Interfaz de usuario con asistentes, progreso y errores. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Interfaz de usuario](user-interface.md)
</dt> <dt>

[Determinar el nivel de la interfaz de usuario a partir de una acción personalizada](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




