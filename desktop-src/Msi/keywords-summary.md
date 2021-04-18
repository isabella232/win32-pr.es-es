---
description: La propiedad Resumen de palabras clave de las bases de datos de instalación o transformaciones contiene una lista de palabras clave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propiedad de Resumen de palabras clave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690668"
---
# <a name="keywords-summary-property"></a>Propiedad de Resumen de palabras clave

La propiedad **Resumen de palabras clave** de las bases de datos de instalación o transformaciones contiene una lista de palabras clave. Los exploradores de archivos pueden usar las palabras clave para realizar búsquedas de palabras clave para un archivo. Esta propiedad contiene una lista de orígenes de la revisión en un paquete de revisión.

Es el autor de una base de datos de instalación, una transformación o un paquete de revisión que proporcione el valor de esta propiedad en la información de resumen. Los autores deben hacer lo siguiente para determinar el valor correcto.

-   En un paquete de instalación, establezca el valor de esta propiedad en una lista de palabras clave. La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.
-   En una transformación, establezca el valor de esta propiedad en una lista de palabras clave. La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.
-   En un paquete de revisión, establezca el valor de esta propiedad en una lista delimitada por signos de punto y coma de ubicaciones de red o direcciones URL para los orígenes de la revisión. Cuando se instala la revisión, el instalador las agrega a la lista de origen del paquete de revisión. Si falta la revisión almacenada en caché, el instalador puede buscar un origen en la ubicación original, una ubicación agregada a la lista de origen mediante la propiedad de **Resumen palabras clave** o una ubicación agregada a la lista de origen mediante las funciones [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




