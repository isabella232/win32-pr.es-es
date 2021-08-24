---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c18c2a3913e8c9e805725f184bd5e969de6272ed05c562799805bd8c74256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725725"
---
# <a name="gestureat-method"></a>Método GestureAt

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Reproduce la animación gestual del carácter especificado en la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). GestureAt_ *  *x,y*



| Parte  | Descripción                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y* | Obligatorio. Valor entero que indica la coordenada de pantalla horizontal *(x*) y la coordenada de pantalla vertical *(y)* a la que se va a gestoar el carácter. Estas coordenadas deben especificarse en píxeles. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El servidor reproduce automáticamente la animación adecuada para hacer gestos hacia la ubicación especificada. Las coordenadas siempre son relativas al origen de la pantalla (parte superior izquierda).

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Además, si la animación asociada no se ha cargado en  el equipo local, el servidor establece la propiedad [**Estado**](status-property.md) del objeto Request en "failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para acceder a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar las animaciones de estado **Gesturing** antes de llamar al **método GestureAt.**

 

 