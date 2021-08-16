---
title: Propiedad Caption (objeto de colección Commands)
description: Obtenga información sobre la propiedad Caption del objeto Colección de comandos. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976707"
---
# <a name="caption-property-commands-collection-object"></a>Propiedad Caption (objeto de colección Commands)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Determina el texto que se muestra para un [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_")._ * [Cadena Commands.Caption](caption-property.md) \[  =  \]



| Parte     | Descripción                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto mostrado como título. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al establecer la propiedad [**Caption**](caption-property.md) de la colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**Visible**](visible-property.md) esté establecida en True y la aplicación no sea el cliente activo de entrada. Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yerba (&) antes de ese carácter.

Si define comandos para una colección [**commands**](/windows/desktop/lwef/the-commands-collection-object) que tiene un [**título**](caption-property.md), normalmente también se define un **título** para su colección **commands** asociada.

 

 
