---
title: Método STOP (características heredadas del entorno de Windows)
description: Stop (Método)
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705107"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Método STOP (características heredadas del entorno de Windows)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Detiene la animación para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Detener_ *  \[ *solicitud*\]



| Parte      | Descripción                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Solicitud* | Opcional. Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) que especifica una llamada de animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea detener. Si no establece el parámetro de **solicitud** , el servidor detiene todas las animaciones para el carácter, incluidas las llamadas [**Get**](get-method.md) en cola, y borra su cola de animación a menos que el carácter esté reproduciendo actualmente la animación que se **oculta** o se **muestra** . Este método no detiene las llamadas **Get** que no estén en cola.

Para detener una animación concreta o una llamada [**Get**](get-method.md) , declare una variable de objeto y asigne la solicitud de animación a esa variable:


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Este método no generará un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Consulte también

[**StopAll (método)**](stopall-method.md)


 

 
