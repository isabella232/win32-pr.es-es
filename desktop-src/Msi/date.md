---
description: La propiedad Date es el mes, el día y el año actuales como una cadena de texto literal en formato MM/DD/AAAA.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653795"
---
# <a name="date-property"></a>Date, propiedad

La propiedad **Date** es el mes, el día y el año actuales como una cadena de texto literal en formato mm/dd/aaaa. Por ejemplo, la fecha 22 de junio de 2005 puede representarse como "06/22/2005". El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con la \_ opción Date fechacorta. El valor de esta propiedad se establece en el Windows Installer y no en el autor del paquete.

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

 

