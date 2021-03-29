---
title: Left (propiedad, Characters, objeto)
description: Left (propiedad)
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105665911"
---
# <a name="left-property-characters-object"></a>Left (propiedad, Characters, objeto)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el borde izquierdo del marco del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ *  \[  =  *Valor* izquierdo\]



| Parte    | Descripción                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Entero largo que especifica el borde izquierdo del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **left** siempre se expresa en píxeles, en relación con el origen de la pantalla (superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.

 

 




