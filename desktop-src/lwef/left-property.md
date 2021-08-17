---
title: Left (propiedad, objeto Characters)
description: Obtenga información sobre la propiedad de objeto Left Characters. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105021"
---
# <a name="left-property-characters-object"></a>Left (propiedad, objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el borde izquierdo del marco del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor_ *  \[  =  *izquierdo*\]



| Parte    | Descripción                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Entero long que especifica el borde izquierdo del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad Left** siempre se expresa en píxeles, en relación con el origen de la pantalla (parte superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.

 

 




