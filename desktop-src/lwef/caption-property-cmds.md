---
title: Propiedad Caption (objeto de colección Commands)
description: Obtenga información sobre la propiedad Caption del objeto Colección de comandos. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262058"
---
# <a name="caption-property-commands-collection-object"></a>Propiedad Caption (objeto de colección Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

## <a name="remarks"></a>Observaciones

Al establecer la propiedad [**Caption**](caption-property.md) de la colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**Visible**](visible-property.md) esté establecida en True y la aplicación no sea el cliente activo de entrada. Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yand (&) delante de ese carácter.

Si define comandos para una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) que tiene un [**título**](caption-property.md), normalmente también se define un título **para** su colección **Commands** asociada.

 

 
