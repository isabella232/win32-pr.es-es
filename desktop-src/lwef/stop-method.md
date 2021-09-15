---
title: Método Stop (características heredadas Windows entorno de ejecución)
description: Stop (Método)
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467219"
---
# <a name="stop-method-legacy-windows-environment-features"></a>Método Stop (características heredadas Windows entorno de ejecución)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Detiene la animación del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Detener_ *  \[ *solicitud*\]



| Parte      | Descripción                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Solicitud* | Opcional. Objeto [**Request**](/windows/desktop/lwef/the-request-object) que especifica una llamada de animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea detener. Si no establece el  parámetro Request, el servidor detiene todas las animaciones del carácter, incluidas las llamadas [**Get**](get-method.md) en  cola, y borra su cola de animación a menos que el carácter esté reproduciendo su animación **Ocultando** o Mostrando. Este método no detiene las llamadas **Get** que no están en cola.

Para detener una animación específica o [**una llamada Get,**](get-method.md) declare una variable de objeto y asigne la solicitud de animación a esa variable:


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



Este método no generará un [**objeto Request.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Consulte también

[**Método StopAll**](stopall-method.md)


 

 
