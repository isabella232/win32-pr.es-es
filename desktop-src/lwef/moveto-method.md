---
title: MoveTo (método)
description: MoveTo (método)
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a245d389bc23d79d9f6cc105fec28ed14f5d511123c1dd113115ff69fc95c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609085"
---
# <a name="moveto-method"></a>MoveTo (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Mueve el carácter especificado a la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). MoveTo_ *  *x,y* \[ *Speed*\]



| Parte    | Descripción                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y*   | Obligatorio. Valor entero que indica el borde izquierdo (*x*) y el borde superior (*y*) del marco de animación. Expresa estas coordenadas en píxeles.                                                   |
| *Velocidad* | Opcional. Valor entero Long que especifica en milisegundos la rapidez con la que se mueve el marco del carácter. El valor predeterminado es 1000. Si se especifica cero (0), se mueve el marco sin reproducir una animación. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El servidor reproduce automáticamente la animación adecuada asignada a los **estados Móviles.** La ubicación de un carácter se basa en la esquina superior izquierda de su marco.

Si declara una variable de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Además, si la animación asociada no se ha cargado en  el equipo local, el servidor establece la propiedad Status del objeto [**Request**](status-property.md) en "failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para acceder a  los datos de caracteres o animaciones, use el método [**Get**](get-method.md) para cargar las animaciones de estado Moving antes de llamar al **método MoveTo.**

Incluso si no se carga la animación, el servidor todavía mueve el marco.

> [!Note]  
> Si llama a **MoveTo** con un valor distinto de cero antes de mostrar el carácter, devolverá un estado de error si le asignó un objeto [**Request,**](/windows/desktop/lwef/the-request-object) porque el valor distinto de cero indica que está intentando reproducir una animación cuando el carácter no está visible.

 

> [!Note]  
> El *efecto* real del parámetro Speed puede variar en función de la velocidad del procesador del equipo y la prioridad de otras tareas que se ejecutan en el sistema.

 

 

 