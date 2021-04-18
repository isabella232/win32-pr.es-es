---
description: ICE24 valida la tabla de propiedades en una base de datos Windows Installer.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193af1e53a3274d1d1307f132fe066ca8940c282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652819"
---
# <a name="ice24"></a>ICE24

ICE24 valida las siguientes propiedades en la [tabla de propiedades](property-table.md):

-   Que la propiedad [**ProductCode**](productcode.md) es un tipo de datos [GUID](guid.md) válido.
-   Que la propiedad [**ProductVersion**](productversion.md) es una versión válida del producto.
-   Que la propiedad [**ProductLanguage**](productlanguage.md) es un tipo de datos de [idioma](language.md) válido.

## <a name="result"></a>Resultado

ICE24 envía un mensaje de error si alguna de estas propiedades no tiene el formato de un tipo de datos válido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



