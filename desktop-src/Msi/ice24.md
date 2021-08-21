---
description: ICE24 valida la tabla Property en una base de datos Windows Installer.
ms.assetid: 1250677b-691e-46bd-83e0-e349106c820b
title: ICE24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3cbeb62285aa9c22a366647dbaeec9e54097a07bb4e876e6bff11bd435cdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528995"
---
# <a name="ice24"></a>ICE24

ICE24 valida las siguientes propiedades en la [tabla Property](property-table.md):

-   Que la [**propiedad ProductCode**](productcode.md) es un tipo de [datos GUID](guid.md) válido.
-   Que la [**propiedad ProductVersion**](productversion.md) es una versión válida del producto.
-   Que la [**propiedad ProductLanguage**](productlanguage.md) es un tipo de datos [language](language.md) válido.

## <a name="result"></a>Resultado

ICE24 publica un mensaje de error si alguna de estas propiedades no tiene el formato de un tipo de datos válido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



