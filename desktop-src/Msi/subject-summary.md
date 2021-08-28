---
description: El valor de la propiedad Resumen del asunto transmite el nombre del producto, la transformación o la revisión que instala el paquete.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propiedad Resumen del asunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9d92328f142e4fd47567e92d4fe3bb7f016b0bf058b2932f7e1136687507e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627235"
---
# <a name="subject-summary-property"></a>Propiedad Resumen del asunto

El valor de la **propiedad Resumen del** asunto transmite el nombre del producto, la transformación o la revisión que instala el paquete.

Es el autor de una base de datos de instalación, una transformación o un paquete de revisión para proporcionar el valor de esta propiedad en la información de resumen. Los autores deben hacer lo siguiente para determinar el valor correcto.

-   Establezca la **propiedad Resumen del asunto** de un paquete de instalación en el mismo valor que la propiedad [**ProductName.**](productname.md)
-   Establezca la **propiedad Resumen del asunto** de una transformación en el mismo valor que la propiedad Resumen **del** sujeto en el paquete de instalación original.
-   Establezca la **propiedad Resumen del asunto** de la información de resumen de un paquete de revisión en una breve descripción de la revisión que incluya el nombre del producto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Resumen de descripciones de propiedades](summary-property-descriptions.md)
</dt> </dl>

 

 




