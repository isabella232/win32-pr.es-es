---
title: Propiedad Description (características heredadas Windows entorno)
description: Description (propiedad)
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7ff293af98303fa0dab97aca76ed169123ea229c1fc70c156ef2c099472157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751997"
---
# <a name="description-property-legacy-windows-environment-features"></a>Propiedad Description (características heredadas Windows entorno)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece una cadena que especifica la descripción del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agente*. **Characters("**_CharacterID_*_"). Cadena de_* \[  =  *descripción*\]



| Parte     | Descripción                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Valor de cadena correspondiente a la descripción del carácter (en la configuración de idioma actual). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La descripción de un **carácter** puede depender de la configuración **de LanguageID del** carácter. El nombre de un carácter en un idioma puede ser diferente o usar caracteres diferentes que en otro. La descripción predeterminada del **carácter** para un idioma específico se define cuando el carácter se compila con el Editor de caracteres del Agente de Microsoft.

> [!Note]  
> El **valor de** la propiedad Description es opcional y no se puede proporcionar para todos los caracteres.

 

 

 




