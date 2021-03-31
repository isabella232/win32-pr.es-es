---
title: Evento de comando
description: Evento de comando
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077721"
---
# <a name="command-event"></a>Evento de comando

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario elige un comando (cliente).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Comando sub** *Agent* \_  **(ByVal** *UserInput ** * *)*



| Parte        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *UserInput* | Identifica el objeto de [**comando**](/windows/desktop/lwef/the-command-object) devuelto por el servidor. <br/> Se puede tener acceso a las siguientes propiedades desde el objeto [**Command**](/windows/desktop/lwef/the-command-object) :<br/> CharacterID <br/> Un valor de cadena que identifica el nombre (ID.) del carácter que ha recibido el comando. <br/> [**Name**](name-property.md)<br/> Un valor de cadena que identifica el nombre (ID.) del comando.<br/> [**Confianza**](confidence-property.md)<br/> Valor entero largo que indica la puntuación de confianza para el comando. <br/> [**Voz**](voice-property.md) <br/> Un valor de cadena que identifica el texto de la voz para el comando.<br/> Alt1Name <br/> Un valor de cadena que identifica el nombre del siguiente comando (segundo) mejor.<br/> Alt1Confidence <br/> Valor entero largo que indica la puntuación de confianza para el siguiente comando (segundo) mejor.<br/> Alt1Voice <br/> Un valor de cadena que identifica el texto de la voz para la siguiente mejor coincidencia de comando alternativa.<br/> Alt2Name <br/> Un valor de cadena que identifica el nombre del tercer comando mejor coincidente.<br/> Alt2Confidence <br/> Un entero largo que identifica la puntuación de confianza para la tercera coincidencia de comando mejor.<br/> Alt2Voice <br/> Un valor de cadena que identifica el texto de la voz para la tercera coincidencia de comando mejor.<br/> [**Contabiliza**](count-property.md) <br/> Valor entero largo que indica el número de alternativas devueltas.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor le informa de este evento cuando la aplicación es de entrada activa y el usuario elige un comando mediante la entrada de voz o el menú emergente del carácter. El evento devuelve el número de comandos coincidentes posibles en el [**recuento**](count-property.md) , así como el nombre, la puntuación de confianza y el texto de la voz de esas coincidencias.

Si la entrada de voz desencadena este evento, el servidor devuelve una cadena que identifica la mejor coincidencia en el parámetro de [**nombre**](name-property.md) , y la segunda y tercera coincidencia en Alt1Name y Alt2Name. Una cadena vacía indica que la entrada no coincidía con ningún comando definido por la aplicación; por ejemplo, podría ser uno de los comandos definidos por el servidor. Si el comando coincidía con el comando del agente; por ejemplo, Hide, se devolvería una cadena vacía en el parámetro **Name** , pero seguiría recibiendo el texto escuchado en el parámetro [**Voice**](voice-property.md) .

Puede obtener el mismo nombre de comando devuelto en más de una entrada. Los parámetros [**Confidence**](confidence-property.md), Alt1Confidence y Alt2Confidence devuelven las puntuaciones relativas, en el intervalo de-100 a 100, devueltos por el motor de reconocimiento de voz para cada coincidencia respectiva. Los parámetros [**Voice**](voice-property.md), Alt1Voice y Alt2Voice devuelven el texto de la voz que coincidía con el motor de reconocimiento de voz para cada alternativa. Si [**Count**](count-property.md) devuelve cero (0), el servidor detectó una entrada de voz, pero determinó que no había ningún comando coincidente.

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, el servidor devuelve el nombre (ID.) del comando seleccionado en la propiedad [**nombre**](name-property.md). También devuelve el valor del parámetro [**Confidence**](confidence-property.md) como 100 y el valor de los parámetros [**Voice**](voice-property.md) como una cadena vacía (""). Alt1Name y Alt2Name también devuelven cadenas vacías. Alt1Confidence y Alt2Confidence devuelven cero (0) y Alt1Voice y Alt2Voice devuelven cadenas vacías. [**Count**](count-property.md) devuelve 1.

> [!Note]  
> No todos los motores de reconocimiento de voz pueden devolver todos los valores de todos los parámetros de este evento. Consulte con el proveedor del motor para determinar si el motor es compatible con la interfaz de Microsoft Speech API para devolver alternativas y puntuaciones de confianza.

 

 

