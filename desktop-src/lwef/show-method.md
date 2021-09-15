---
title: Show (método)
description: Show (método)
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468783"
---
# <a name="show-method"></a>Show (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Hace que el carácter especificado sea visible y reproduce su animación **Showing** asociada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Mostrar_ *  \[ *rápido*\]



| Parte   | Descripción                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Expresión booleana que especifica si el servidor reproduce la **animación Mostrando.** **True** Omite la animación **Mostrar** estado. <br/> **False** (valor predeterminado) No omite la animación **Mostrar** estado. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Además, si no se ha cargado la [](status-property.md) animación **Showing** asociada y no se ha  especificado el parámetro **Fast** como **True**, el servidor establece la propiedad Status del objeto Request en "failed" con un número de error adecuado. Por lo tanto, si usa el protocolo HTTP para tener acceso  a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación de estado Mostrando antes de llamar al **método Show.**

Evite establecer el **parámetro Fast** en **True sin** reproducir primero una animación de antemano; De lo contrario, el marco de caracteres puede mostrarse sin ninguna imagen. En concreto, tenga en cuenta que si llama a [**MoveTo**](moveto-method.md) cuando el carácter no está visible, no reproducirá ninguna animación. Por lo tanto, si llama al **método Show** con **Fast** establecido en **True,** no se mostrará ninguna imagen. Del mismo modo, si llama a [**Ocultar,**](hide-method.md) **mostrar** con **rápido** establecido en **True**, no habrá ninguna imagen visible.

## <a name="see-also"></a>Consulte también

[**Hide (método)**](hide-method.md)


 

