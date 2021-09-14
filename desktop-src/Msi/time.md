---
description: La propiedad Time es la hora actual en horas, minutos y segundos como una cadena de texto literal con el formato HH:MM:SS con un reloj de 24 horas.
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propiedad Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169685"
---
# <a name="time-property"></a>Propiedad Time

La **propiedad Time** es la hora actual en horas, minutos y segundos como una cadena de texto literal con el formato HH:MM:SS con un reloj de 24 horas. Por ejemplo, la hora 6:57 p.m. se representa mediante "18:57:00". El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante la función [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con la opción \_ TIME FORCE24HOURFORMAT \| TIME \_ NOTIMEMARKER. El valor de esta propiedad lo establece el instalador Windows y no el autor del paquete.

## <a name="remarks"></a>Observaciones

Dado que se trata de una cadena de texto, no se puede usar en expresiones condicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
