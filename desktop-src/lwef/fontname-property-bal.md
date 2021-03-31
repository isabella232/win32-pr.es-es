---
title: FontName (propiedad, objeto Balloon)
description: FontName (propiedad)
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149820"
---
# <a name="fontname-property-balloon-object"></a>FontName (propiedad, objeto Balloon)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece la fuente utilizada en el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Fuente Balloon. FontName_ *  \[  =  \]



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *tipo* | Valor de cadena que corresponde al nombre de la fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad [**FontName**](fontname-property.md) define la fuente utilizada para mostrar texto en la ventana de globo de palabras de una cadena. El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft. Además, el usuario puede invalidar la configuración de fuente para todos los caracteres de la hoja de propiedades del agente de Microsoft.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si usa un carácter que no ha compilado, compruebe las propiedades [**FontName**](fontname-property.md) y [**FontCharSet**](fontcharset-property.md) del carácter para determinar si son adecuados para la configuración regional. Es posible que tenga que establecer estos valores antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.

 

 

 




