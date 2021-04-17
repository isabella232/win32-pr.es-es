---
description: El valor de la propiedad Resumen de asunto transmite el nombre del producto, la transformación o el parche que instala el paquete.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propiedad de Resumen de asunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653564"
---
# <a name="subject-summary-property"></a>Propiedad de Resumen de asunto

El valor de la propiedad **Resumen de asunto** transmite el nombre del producto, la transformación o el parche que instala el paquete.

Es el autor de una base de datos de instalación, una transformación o un paquete de revisión que proporcione el valor de esta propiedad en la información de resumen. Los autores deben hacer lo siguiente para determinar el valor correcto.

-   Establezca la propiedad **Resumen de asunto** de un paquete de instalación en el mismo valor que la propiedad [**ProductName**](productname.md) .
-   Establezca la propiedad **Resumen del asunto** en una transformación en el mismo valor que la propiedad Resumen del **firmante** en el paquete de instalación original.
-   Establezca la propiedad **Resumen del asunto** en la información de Resumen de un paquete de revisión en una breve descripción de la revisión que incluye el nombre del producto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




