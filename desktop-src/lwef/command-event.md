---
title: Evento command
description: Evento command
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567573"
---
# <a name="command-event"></a>Evento command

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario elige un comando (cliente).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent* \_ **(Comando,** **ByVal** *UserInput...))**



| Parte        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *UserInput* | Identifica el objeto [**Command**](/windows/desktop/lwef/the-command-object) devuelto por el servidor. <br/> Se puede acceder a las siguientes propiedades desde el [**objeto Command:**](/windows/desktop/lwef/the-command-object)<br/> CharacterID <br/> Valor de cadena que identifica el nombre (id.) del carácter que recibió el comando. <br/> [**Nombre**](name-property.md)<br/> Valor de cadena que identifica el nombre (id.) del comando.<br/> [**Confianza**](confidence-property.md)<br/> Valor entero Long que indica la puntuación de confianza para el comando. <br/> [**Voz**](voice-property.md) <br/> Valor de cadena que identifica el texto de voz del comando.<br/> Alt1Name <br/> Valor de cadena que identifica el nombre del siguiente (segundo) mejor comando.<br/> Alt1Confidence <br/> Valor entero Long que indica la puntuación de confianza para el siguiente (segundo) mejor comando.<br/> Alt1Voice <br/> Valor de cadena que identifica el texto de voz para la siguiente mejor coincidencia de comando alternativa.<br/> Alt2Name <br/> Valor de cadena que identifica el nombre de la tercera mejor coincidencia de comandos.<br/> Alt2Confidence <br/> Entero Largo que identifica la puntuación de confianza para la tercera mejor coincidencia de comandos.<br/> Alt2Voice <br/> Valor de cadena que identifica el texto de voz para la tercera mejor coincidencia de comandos.<br/> [**Contar**](count-property.md) <br/> Valor entero largo que indica el número de alternativas devueltas.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor le notifica este evento cuando la aplicación está activa en la entrada y el usuario elige un comando por entrada hablada o menú emergente del carácter. El evento pasa el número de posibles comandos de coincidencia en [**Count,**](count-property.md) así como el nombre, la puntuación de confianza y el texto de voz para esas coincidencias.

Si la entrada de voz desencadena este evento, el servidor devuelve una cadena que identifica la mejor coincidencia en el parámetro [**Name**](name-property.md) y la segunda y la tercera mejor coincidencia en Alt1Name y Alt2Name. Una cadena vacía indica que la entrada no coincide con ningún comando definido por la aplicación; por ejemplo, podría ser uno de los comandos definidos del servidor. Si el comando coincidió con el comando del agente; Por ejemplo, Ocultar, se devolvería una cadena vacía en el parámetro **Name,** pero seguiría recibiendo el texto que se escucha en el [**parámetro Voice.**](voice-property.md)

Puede obtener el mismo nombre de comando devuelto en más de una entrada. [**Los**](confidence-property.md)parámetros Confidence , Alt1Confidence y Alt2Confidence devuelven las puntuaciones relativas, en el intervalo de -100 a 100, que devuelve el motor de reconocimiento de voz para cada coincidencia respectiva. [**Los parámetros Voice**](voice-property.md), Alt1Voice y Alt2Voice devuelven el texto de voz con el que coincidió el motor de reconocimiento de voz para cada alternativa. Si [**Count**](count-property.md) devuelve cero (0), el servidor detectó la entrada hablada, pero determinó que no había ningún comando correspondiente.

Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario seleccionó el comando en el menú emergente del carácter, el servidor devuelve el nombre (id.) del comando seleccionado en la [**propiedad Nombre.**](name-property.md) También devuelve el valor del parámetro [**Confidence**](confidence-property.md) como 100 y el valor de los parámetros [**voice**](voice-property.md) como la cadena vacía (""). Alt1Name y Alt2Name también devuelven cadenas vacías. Alt1Confidence y Alt2Confidence devuelven cero (0) y Alt1Voice y Alt2Voice devuelven cadenas vacías. [**Count**](count-property.md) devuelve 1.

> [!Note]  
> No todos los motores de reconocimiento de voz pueden devolver todos los valores de todos los parámetros de este evento. Consulte con el proveedor del motor para determinar si el motor admite la interfaz Speech API Microsoft para devolver alternativas y puntuaciones de confianza.

 

 

