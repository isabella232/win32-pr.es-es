---
title: Show (método)
description: Show (método)
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704938"
---
# <a name="show-method"></a>Show (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Hace que el carácter especificado sea visible y reproduzca la animación **mostrada** asociada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Mostrar* *  \[ *rápido*\]



| Parte   | Descripción                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Una expresión booleana que especifica si el servidor reproduce la animación **que se muestra** . **True** Omite la animación de estado **que se muestra** . <br/> **False** (valor predeterminado) no omite la animación de estado **que se muestra** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si la animación **que se muestra** asociada no se ha cargado y no se ha especificado el parámetro **Fast** como **true**, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación de estado **que se muestra** antes de llamar al método **Show** .

Evite establecer el parámetro **Fast** en **true** sin reproducir primero una animación de antemano; de lo contrario, el marco de caracteres puede mostrarse sin ninguna imagen. En concreto, tenga en cuenta que si llama a [**moveTo**](moveto-method.md) cuando el carácter no está visible, no se reproduce ninguna animación. Por lo tanto, si llama al método **Show** con **Fast** establecido en **true**, no se mostrará ninguna imagen. Del mismo modo, si llama a [**Hide**](hide-method.md) y **Show** con **Fast** set en **true**, no habrá ninguna imagen visible.

## <a name="see-also"></a>Consulte también

[**Hide (método)**](hide-method.md)


 

