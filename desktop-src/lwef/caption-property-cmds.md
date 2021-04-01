---
title: Propiedad Caption (objeto de colección Commands)
description: Propiedad Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149797"
---
# <a name="caption-property-commands-collection-object"></a>Propiedad Caption (objeto de colección Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Determina el texto que se muestra para un objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ * [Commands. Caption](caption-property.md) ( \[  =  *cadena* )\]



| Parte     | Descripción                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto que se muestra como título. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al establecer la propiedad [**Caption**](caption-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**visible**](visible-property.md) esté establecida en true y la aplicación no sea el cliente de entrada-activo. Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.

Si define comandos para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tiene un [**título**](caption-property.md), normalmente también se define un **título** para la colección de **comandos** asociada.

 

 
