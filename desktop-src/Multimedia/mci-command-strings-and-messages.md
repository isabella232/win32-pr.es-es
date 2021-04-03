---
title: Mensajes y cadenas de comandos MCI
description: Mensajes y cadenas de comandos MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Cadenas de comandos MCI, acerca de
- Mensajes de comandos de MCI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904608"
---
# <a name="mci-command-strings-and-messages"></a>Mensajes y cadenas de comandos MCI

MCI admite [cadenas de comandos](command-strings.md) y [mensajes de comandos](command-messages.md). Puede usar cadenas o mensajes, o ambos, en la aplicación MCI.

-   La *interfaz de mensajes de comandos* consta de constantes y estructuras. Use la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar mensajes a un dispositivo MCI.
-   La *interfaz de cadena de comandos* proporciona una versión textual de los mensajes de comandos. Use la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) para enviar cadenas a un dispositivo MCI. Las cadenas de comandos duplican la funcionalidad de los mensajes de comandos. El sistema operativo convierte las cadenas de comandos en mensajes de comandos antes de enviarlos al controlador MCI para su procesamiento.

Los mensajes de comandos que recuperan información lo hacen en forma de estructuras, que son fáciles de interpretar en una aplicación de C. Estas estructuras pueden contener información sobre muchos aspectos diferentes de un dispositivo. Las cadenas de comandos que recuperan información lo hacen en forma de cadenas y solo pueden recuperar una cadena cada vez. La aplicación debe analizar o probar cada cadena para interpretarla. Es posible que los mensajes de comando sean más fáciles de usar que las cadenas de comandos en algunos casos, pero las cadenas de comandos son fáciles de recordar e implementar. Algunas aplicaciones MCI usan cadenas de comandos cuando el valor devuelto no se usará (excepto para comprobar que se ha realizado correctamente) y mensajes de comando al recuperar información del dispositivo.

Cuando se analizan los comandos, en esta información general se usa el formato de cadena del comando seguido del formulario de mensaje entre paréntesis.

 

 