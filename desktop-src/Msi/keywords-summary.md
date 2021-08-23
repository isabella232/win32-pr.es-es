---
description: La propiedad Resumen de palabras clave de las bases de datos o transformaciones de instalación contiene una lista de palabras clave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propiedad Resumen de palabras clave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680315"
---
# <a name="keywords-summary-property"></a>Propiedad Resumen de palabras clave

La **propiedad Resumen de palabras** clave de las bases de datos o transformaciones de instalación contiene una lista de palabras clave. Los exploradores de archivos pueden usar las palabras clave para realizar búsquedas de palabras clave en un archivo. Esta propiedad contiene una lista de orígenes de la revisión en un paquete de revisión.

Es el autor de una base de datos de instalación, una transformación o un paquete de revisión para proporcionar el valor de esta propiedad en la información de resumen. Los autores deben hacer lo siguiente para determinar el valor correcto.

-   En un paquete de instalación, establezca el valor de esta propiedad en una lista de palabras clave. La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.
-   En una transformación, establezca el valor de esta propiedad en una lista de palabras clave. La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.
-   En un paquete de revisión, establezca el valor de esta propiedad en una lista delimitada por punto y coma de ubicaciones de red o dirección URL para los orígenes de la revisión. Cuando se instala la revisión, el instalador los agrega a la lista de origen del paquete de revisión. Si falta la revisión almacenada en caché, el instalador puede buscar un origen en la ubicación original, una ubicación agregada a la lista de origen por la propiedad **Resumen** de palabras clave o una ubicación agregada a la lista de origen mediante las funciones [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Resumen de descripciones de propiedades](summary-property-descriptions.md)
</dt> </dl>

 

 




