---
description: La propiedad Date es el mes, día y año actuales como una cadena de texto literal con el formato MM/DD/YYYY.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf76df99c5567351ddd4d36d1aaad56c8a4d1f385f21ca977a4d54916ce99a4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129635"
---
# <a name="date-property"></a>Date, propiedad

La **propiedad Date** es el mes, día y año actuales como una cadena de texto literal con el formato MM/DD/YYYY. Por ejemplo, la fecha del 22 de junio de 2005 puede representarse como "22/06/2005". El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con la opción DATE \_ SHORTDATE. El valor de esta propiedad lo establece el instalador Windows y no el autor del paquete.

## <a name="remarks"></a>Comentarios

Dado que se trata de una cadena de texto, no se puede usar en expresiones condicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

