---
title: Propiedad Description (características heredadas del entorno de Windows)
description: Description (propiedad)
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078704"
---
# <a name="description-property-legacy-windows-environment-features"></a>Propiedad Description (características heredadas del entorno de Windows)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece una cadena que especifica la descripción del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente*. **Caracteres ("**_CharacterID_*_")._* \[  =  *Cadena* de Descripción\]



| Parte     | Descripción                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Un valor de cadena correspondiente a la descripción del carácter (en la configuración de idioma actual). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **Descripción** de un carácter puede depender del valor de **LanguageID** del carácter. El nombre de un carácter en un idioma puede ser diferente o utilizar caracteres distintos a los de otro. La **Descripción** predeterminada del carácter para un idioma específico se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

> [!Note]  
> El valor de la propiedad **Description** es opcional y es posible que no se proporcione para todos los caracteres.

 

 

 




