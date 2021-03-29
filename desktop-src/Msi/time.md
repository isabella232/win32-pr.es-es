---
description: 'La propiedad Time es la hora actual en horas, minutos y segundos como una cadena de texto literal en el formato HH: MM: SS con un reloj de 24 horas.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propiedad Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680560"
---
# <a name="time-property"></a>Propiedad Time

La propiedad **Time** es la hora actual en horas, minutos y segundos como una cadena de texto literal en el formato HH: mm: SS con un reloj de 24 horas. Por ejemplo, la hora 6:57 p.m. se representa mediante "18:57:00". El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante la función [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con la opción Time \_ FORCE24HOURFORMAT \| Time \_ NOTIMEMARKER. El valor de esta propiedad se establece en el Windows Installer y no en el autor del paquete.

## <a name="remarks"></a>Observaciones

Dado que se trata de una cadena de texto, no se puede usar en expresiones condicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
