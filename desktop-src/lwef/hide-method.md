---
title: Hide (método)
description: Hide (método)
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258036"
---
# <a name="hide-method"></a>Hide (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Oculta el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Ocultar_ *  \[ *rápido*\]



| Parte   | Descripción                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Un valor booleano que indica si se omite la animación asociada al estado Ocultar true del carácter **No** se reproduce la **animación Ocultar.** <br/> **False** (valor predeterminado) Reproduce la **animación Ocultar.** <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor pone en cola las acciones del método **Hide** en la cola del carácter, por lo que puede usarlo para ocultar el carácter después de una secuencia de otras animaciones. Puede reproducir la acción inmediatamente mediante el método [**Stop**](stop-method.md) antes de llamar a este método.

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Además, si no se ha cargado la animación **oculta** asociada y no se ha especificado el parámetro **Fast** como **True**, el servidor establece la propiedad Request **object** [**Status**](status-property.md) en "failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para tener acceso a datos de caracteres o animaciones, use el método [**Get**](get-method.md) y especifique el estado **Ocultar** para cargar la animación antes de llamar **al método Hide.**

Ocultar un carácter también puede provocar que se desencadene [**el evento ActivateInput**](activateinput-event.md) de otro cliente.

> [!Note]  
> Los caracteres ocultos no pueden acceder al canal de audio. El servidor pasará un estado de error en el evento [**RequestComplete**](requestcomplete-event.md) si genera una solicitud de animación y el carácter está oculto.

 

## <a name="see-also"></a>Consulte también

[**Show (método)**](show-method.md)


 

