---
title: Método play (características heredadas del entorno de Windows)
description: Play (método)
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695816"
---
# <a name="play-method-legacy-windows-environment-features"></a>Método play (características heredadas del entorno de Windows)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Reproduce la animación especificada para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Reproducir_* "*AnimationName*"

</dd> </dl> 

| Parte            | Descripción                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | Obligatorio. Cadena que especifica el nombre de una secuencia de animación. |



 

## <a name="remarks"></a>Observaciones

El nombre de una animación se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft. Antes de reproducir la animación especificada, el servidor intenta reproducir la animación de **retorno** de la animación anterior, si se ha asignado una.

Al tener acceso a las animaciones de un carácter mediante un protocolo de archivo convencional, puede simplemente usar el método **Play** especificando el nombre de la animación. Sin embargo, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método **Get** para cargar la animación antes de llamar al método **Play** .

Para obtener más información, vea el método **Get** .

Para simplificar la sintaxis, puede declarar una referencia de objeto y establecerla para que haga referencia al objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) y use la referencia como parte de las instrucciones de **reproducción** :


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si especifica una animación que no está cargada o si el carácter no se ha cargado correctamente, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de error adecuado. Sin embargo, si la animación no existe y los datos del carácter ya se han cargado correctamente, el servidor genera un error.

El método **Play** no hace que el carácter esté visible. Si el carácter no está visible, el servidor reproduce la animación de manera invisible y establece la propiedad [**status**](status-property.md) del objeto [**request**](/windows/desktop/lwef/the-request-object) .

 

 
