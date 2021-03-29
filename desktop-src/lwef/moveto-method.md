---
title: MoveTo (método)
description: MoveTo (método)
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077753"
---
# <a name="moveto-method"></a>MoveTo (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Mueve el carácter especificado a la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). MoveTo* *  *velocidad x, y* \[ \]



| Parte    | Descripción                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Obligatorio. Un valor entero que indica el borde izquierdo (*x*) y el borde superior (*y*) del fotograma de animación. Exprese estas coordenadas en píxeles.                                                   |
| *Velocidad* | Opcional. Valor entero largo que especifica en milisegundos la rapidez con la que se mueve el marco del carácter. El valor predeterminado es 1000. Si se especifica cero (0), se mueve el marco sin reproducir una animación. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor reproduce automáticamente la animación adecuada asignada a los Estados **móviles** . La ubicación de un carácter se basa en la esquina superior izquierda de su marco.

Si declara una variable de objeto y la establece en este método, devolverá un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si la animación asociada no se ha cargado en el equipo local, el servidor establece la propiedad de [**Estado**](status-property.md) del objeto de **solicitud** en "Failed" con un número de error adecuado. Por consiguiente, si usa el protocolo HTTP para tener acceso a los datos de caracteres o de animación, use el método [**Get**](get-method.md) para cargar las animaciones de estado en **movimiento** antes de llamar al método **moveTo** .

Incluso si la animación no está cargada, el servidor todavía mueve el marco.

> [!Note]  
> Si llama a **moveTo** con un valor distinto de cero antes de que se muestre el carácter, devolverá un estado de error si le asignó un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) , ya que el valor distinto de cero indica que está intentando reproducir una animación cuando el carácter no está visible.

 

> [!Note]  
> El efecto real del parámetro de *velocidad* puede variar en función de la velocidad del procesador del equipo y la prioridad de otras tareas que se ejecutan en el sistema.

 

 

 