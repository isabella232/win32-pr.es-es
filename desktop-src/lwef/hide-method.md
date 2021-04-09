---
title: Hide (método)
description: Hide (método)
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149236"
---
# <a name="hide-method"></a>Hide (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Oculta el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Ocultar* *  \[ *rápidamente*\]



| Parte   | Descripción                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Un valor booleano que indica si se va a omitir la animación asociada al estado de ocultación del carácter **true** no reproduce la animación de **ocultación** . <br/> **False** (valor predeterminado) reproduce la animación de **ocultación** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor pone en cola las acciones del método **Hide** en la cola del carácter, por lo que puede usarla para ocultar el carácter después de una secuencia de otras animaciones. Puede reproducir la acción inmediatamente mediante el método [**Stop**](stop-method.md) antes de llamar a este método.

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si la animación de **ocultación** asociada no se ha cargado y no se ha especificado el parámetro **Fast** como **true**, el servidor establece la propiedad de [**Estado**](status-property.md) de objeto de **solicitud** en "Failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para tener acceso a los datos de caracteres o de animación, use el método [**Get**](get-method.md) y especifique el estado de **ocultación** para cargar la animación antes de llamar al método **Hide** .

Ocultar un carácter también puede producir el desencadenamiento del evento [**ActivateInput**](activateinput-event.md) de otro cliente.

> [!Note]  
> Los caracteres ocultos no pueden tener acceso al canal de audio. El servidor devolverá un estado de error en el evento [**RequestComplete**](requestcomplete-event.md) si genera una solicitud de animación y el carácter está oculto.

 

## <a name="see-also"></a>Consulte también

[**Show (método)**](show-method.md)


 

