---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487563"
---
# <a name="gestureat-method"></a>Método GestureAt

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Reproduce la animación gesturing para el carácter especificado en la ubicación especificada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). GestureAt* *  *x, y*



| Parte  | Descripción                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Obligatorio. Valor entero que indica la coordenada de pantalla horizontal (*x*) y la coordenada de pantalla vertical (*y*) a la que se moverá el carácter. Estas coordenadas se deben especificar en píxeles. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor reproduce automáticamente la animación adecuada para gestos hacia la ubicación especificada. Las coordenadas siempre se relacionan con el origen de la pantalla (superior izquierda).

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si la animación asociada no se ha cargado en el equipo local, el servidor establece la propiedad de [**Estado**](status-property.md) del objeto de **solicitud** en "Failed" con un número de error adecuado. Por consiguiente, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar las animaciones de estado de **gesturing** antes de llamar al método **GestureAt** .

 

 