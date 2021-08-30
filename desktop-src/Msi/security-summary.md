---
description: La propiedad Resumen de seguridad indica si el paquete debe abrirse como de solo lectura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propiedad Resumen de seguridad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a91d66379c06ec1378e1410453fb4014761e0f15145453fe17afb3b65bafbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040725"
---
# <a name="security-summary-property"></a>Propiedad Resumen de seguridad

La **propiedad Resumen de** seguridad indica si el paquete debe abrirse como de solo lectura. La herramienta de edición de bases de datos no debe modificar una base de datos aplicada de solo lectura y debe emitir una advertencia en los intentos de modificar una base de datos recomendada de solo lectura. Los siguientes valores de esta propiedad son aplicables a los Windows instalador.



| Value | Descripción           |
|-------|-----------------------|
| 0     | Sin restricción        |
| 2     | Se recomienda solo lectura |
| 4     | Aplicación de solo lectura    |



 

Esta propiedad debe establecerse en recomendado de solo lectura (2) para una base de datos de instalación y en se aplica de solo lectura (4) para una transformación o revisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Resumen de descripciones de propiedades](summary-property-descriptions.md)
</dt> </dl>

 

 




