---
description: La propiedad Resumen de seguridad transmite si el paquete debe abrirse como de solo lectura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propiedad de Resumen de seguridad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653872"
---
# <a name="security-summary-property"></a>Propiedad de Resumen de seguridad

La propiedad **Resumen de seguridad** transmite si el paquete debe abrirse como de solo lectura. La herramienta de edición de bases de datos no debe modificar una base de datos forzada de solo lectura y debe emitir una advertencia en los intentos de modificar una base de datos recomendada de solo lectura. Los siguientes valores de esta propiedad se aplican a los archivos Windows Installer.



| Value | Descripción           |
|-------|-----------------------|
| 0     | Sin restricción        |
| 2     | Recomendado solo lectura |
| 4     | Solo lectura forzada    |



 

Esta propiedad debe establecerse en solo lectura recomendado (2) para una base de datos de instalación y en la aplicación de solo lectura (4) para una transformación o revisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




