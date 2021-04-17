---
description: El instalador establece la última propiedad guardada por Resumen en un valor que depende de si se trata de un paquete de instalación, una transformación o un paquete de revisión. En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad LogonUser durante una instalación administrativa. Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación. Esta propiedad debe establecerse en null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla. En una transformación, esta propiedad de Resumen contiene los IDENTIFICADOres de plataforma e idioma que debe tener una base de datos una vez transformada. La propiedad especifica en qué se debe establecer el Resumen de la plantilla en la nueva base de datos. En un paquete de revisión, esta propiedad de Resumen contiene una lista delimitada por signos de punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última vez que se guardó la propiedad Summary
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690666"
---
# <a name="last-saved-by-summary-property"></a>Última vez que se guardó la propiedad Summary

El instalador establece la **última propiedad guardada por Resumen** en un valor que depende de si se trata de un paquete de instalación, una transformación o un paquete de revisión.

En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad [**LogonUser**](logonuser.md) durante una [instalación administrativa](administrative-installation.md). Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación. Esta propiedad debe establecerse en null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.

En una transformación, esta propiedad de Resumen contiene los IDENTIFICADOres de plataforma e idioma que debe tener una base de datos una vez transformada. La propiedad especifica en qué se debe establecer el Resumen de la [**plantilla**](template-summary.md) en la nueva base de datos.

En un paquete de revisión, esta propiedad de Resumen contiene una lista delimitada por signos de punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




