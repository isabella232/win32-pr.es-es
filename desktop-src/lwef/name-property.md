---
title: Propiedad Name (objeto Characters)
description: Obtenga información sobre la propiedad Name del objeto Characters. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08509d5d2a349c56548259db4846203da6f632ff76c86309db87e6aa90583a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608655"
---
# <a name="name-property-characters-object"></a>Propiedad Name (objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece una cadena que especifica el nombre predeterminado del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Cadena de_ *  \[  =  *nombre*\]



| Parte     | Descripción                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Valor de cadena correspondiente al nombre del carácter (en la configuración de idioma actual). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El nombre de **un carácter** puede depender de la configuración [**de LanguageID del**](languageid-property.md) carácter. El nombre de un carácter en un idioma puede ser diferente o usar caracteres diferentes que en otro. El nombre predeterminado del **carácter para** un idioma específico se define cuando el carácter se compila con el Editor de caracteres del agente de Microsoft.

Evite cambiar el nombre de un carácter, especialmente cuando se usa en un escenario en el que otras aplicaciones cliente pueden usar el mismo carácter. Además, el Agente usa el nombre del carácter **para** crear automáticamente comandos para ocultar y mostrar el carácter.

 

 




