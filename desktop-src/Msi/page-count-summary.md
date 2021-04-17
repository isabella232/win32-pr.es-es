---
description: La propiedad de Resumen de recuento de páginas contiene la versión de instalador mínima que requiere el paquete de instalación.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propiedad de Resumen de recuento de páginas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653769"
---
# <a name="page-count-summary-property"></a>Propiedad de Resumen de recuento de páginas

La propiedad de **Resumen de recuento de páginas** contiene la versión de instalador mínima que requiere el paquete de instalación. Para un mínimo de Windows Installer 2,0, esta propiedad se debe establecer en el entero 200. Para un mínimo de Windows Installer 3,0, esta propiedad se debe establecer en el entero 300. Para un mínimo de Windows Installer 3,1, esta propiedad debe establecerse en 301. Para un mínimo de Windows Installer 4,5, esta propiedad debe establecerse en 405. Para un mínimo de Windows Installer 5,0, esta propiedad debe establecerse en 500.

En el caso de los [paquetes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), esta propiedad se debe establecer en el entero 200 o superior. En el caso de los paquetes de Windows Installer de 64 bits en la plataforma Arm64, esta propiedad se debe establecer en el entero 500 o superior.

En el caso de un paquete de transformación, la propiedad de **Resumen de recuento de páginas** contiene la versión de instalador mínima necesaria para procesar la transformación. Se establece en el mayor de los dos valores de propiedad de **Resumen de recuento de páginas** que pertenecen a las bases de datos utilizadas para generar la transformación.

En el caso de un paquete de revisión, la propiedad de **Resumen de recuento de páginas** está establecida en NULL.

Esta propiedad de resumen es obligatoria.

Esta propiedad se puede usar para crear un paquete que solo pueda instalarse en la versión mínima o posterior especificada del Windows Installer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




