---
description: El instalador establece la propiedad Last Saved by Summary en un valor que depende de si se trata de un paquete de instalación, transformación o revisión. En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad LogonUser durante una instalación administrativa. Los desarrolladores de herramientas de edición de bases de datos pueden usar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modifique la base de datos de instalación. Esta propiedad debe establecerse en Null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla. En una transformación, esta propiedad de resumen contiene los identificadores de plataforma e idioma que debe tener una base de datos después de que se haya transformado. La propiedad especifica en qué se debe establecer el resumen de plantilla en la nueva base de datos. En un paquete de revisión, esta propiedad de resumen contiene una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última propiedad Guardada por resumen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071983"
---
# <a name="last-saved-by-summary-property"></a>Última propiedad Guardada por resumen

El instalador establece la **propiedad Last Saved by Summary** en un valor que depende de si se trata de un paquete de instalación, transformación o revisión.

En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad [**LogonUser**](logonuser.md) durante una [instalación administrativa.](administrative-installation.md) Los desarrolladores de herramientas de edición de bases de datos pueden usar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modifique la base de datos de instalación. Esta propiedad debe establecerse en Null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.

En una transformación, esta propiedad de resumen contiene los identificadores de plataforma e idioma que debe tener una base de datos después de que se haya transformado. La propiedad especifica en qué se debe establecer [**el resumen de**](template-summary.md) plantilla en la nueva base de datos.

En un paquete de revisión, esta propiedad de resumen contiene una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Descripciones de propiedades de resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




