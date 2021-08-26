---
description: El instalador establece la propiedad Último guardado por resumen en un valor que depende de si se trata de un paquete de instalación, transformación o paquete de revisión. En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad LogonUser durante una instalación administrativa. Los desarrolladores de herramientas de edición de bases de datos pueden usar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modifique la base de datos de instalación. Esta propiedad debe establecerse en Null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla. En una transformación, esta propiedad de resumen contiene los identificadores de plataforma e idioma que debe tener una base de datos después de transformarla. La propiedad especifica en qué se debe establecer el resumen de plantilla en la nueva base de datos. En un paquete de revisión, esta propiedad de resumen contiene una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última propiedad Guardado por resumen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9299dc6a00af4e48eb3901842aba58a3c8d9a9c1d98d3a3e1e0f05bfccc4333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979455"
---
# <a name="last-saved-by-summary-property"></a>Última propiedad Guardado por resumen

El instalador establece la **propiedad Último** guardado por resumen en un valor que depende de si se trata de un paquete de instalación, transformación o paquete de revisión.

En un paquete de instalación, el instalador establece esta propiedad en el valor de la propiedad [**LogonUser**](logonuser.md) durante una [instalación administrativa.](administrative-installation.md) Los desarrolladores de herramientas de edición de bases de datos pueden usar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modifique la base de datos de instalación. Esta propiedad debe establecerse en Null en una base de datos de envío final. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.

En una transformación, esta propiedad de resumen contiene los identificadores de plataforma e idioma que debe tener una base de datos después de transformarla. La propiedad especifica en qué se debe establecer [**el resumen**](template-summary.md) de plantilla en la nueva base de datos.

En un paquete de revisión, esta propiedad de resumen contiene una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Resumen de descripciones de propiedades](summary-property-descriptions.md)
</dt> </dl>

 

 




