---
description: La propiedad Resumen de recuento de páginas contiene la versión mínima del instalador requerida por el paquete de instalación.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propiedad Resumen de recuento de páginas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250934"
---
# <a name="page-count-summary-property"></a>Propiedad Resumen de recuento de páginas

La **propiedad Resumen de recuento de** páginas contiene la versión mínima del instalador requerida por el paquete de instalación. Para un mínimo de Windows Installer 2.0, esta propiedad debe establecerse en el entero 200. Para un mínimo de Windows Installer 3.0, esta propiedad debe establecerse en el entero 300. Para un mínimo de Windows Installer 3.1, esta propiedad debe establecerse en 301. Para un mínimo de Windows Installer 4.5, esta propiedad debe establecerse en 405. Para un mínimo de Windows Installer 5.0, esta propiedad debe establecerse en 500.

En el caso de los paquetes Windows instalador de [64](64-bit-windows-installer-packages.md)bits, esta propiedad debe establecerse en el entero 200 o superior. Para paquetes de instalador de Windows de 64 bits en la plataforma Arm64, esta propiedad debe establecerse en el entero 500 o superior.

Para un paquete de transformación, la **propiedad Resumen de recuento** de páginas contiene la versión mínima del instalador necesaria para procesar la transformación. Establezca en el mayor de los dos valores de propiedad **Resumen de recuento** de páginas que pertenecen a las bases de datos utilizadas para generar la transformación.

Para un paquete de revisión, la **propiedad Resumen de recuento de** páginas está establecida en Null.

Esta propiedad de resumen es obligatoria.

Esta propiedad se puede usar para crear un paquete que solo se puede instalar con la versión mínima o posterior especificada del instalador de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




