---
title: Mensajes y cadenas de comandos de MCI
description: Mensajes y cadenas de comandos de MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Cadenas de comandos de MCI, acerca de
- Mensajes de comando de MCI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476846"
---
# <a name="mci-command-strings-and-messages"></a>Mensajes y cadenas de comandos de MCI

MCI admite [cadenas de comandos y](command-strings.md) [mensajes de comando.](command-messages.md) Puede usar cadenas o mensajes, o ambos, en la aplicación MCI.

-   La *interfaz de mensaje de comando* consta de constantes y estructuras. Use la [**función mciSendCommand para**](/previous-versions//dd757160(v=vs.85)) enviar mensajes a un dispositivo MCI.
-   La *interfaz de cadena de comandos* proporciona una versión textual de los mensajes de comando. Use la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) para enviar cadenas a un dispositivo MCI. Las cadenas de comandos duplican la funcionalidad de los mensajes de comando. El sistema operativo convierte las cadenas de comando en mensajes de comando antes de enviarlos al controlador MCI para su procesamiento.

Los mensajes de comando que recuperan información lo hacen en forma de estructuras, que son fáciles de interpretar en una aplicación de C. Estas estructuras pueden contener información sobre muchos aspectos diferentes de un dispositivo. Las cadenas de comandos que recuperan información lo hacen en forma de cadenas y solo pueden recuperar una cadena a la vez. La aplicación debe analizar o probar cada cadena para interpretarla. Es posible que los mensajes de comando sean más fáciles de usar que las cadenas de comandos en algunos casos, pero las cadenas de comando son fáciles de recordar e implementar. Algunas aplicaciones MCI usan cadenas de comandos cuando no se usará el valor devuelto (que no sea para comprobar que se ha correcto) y mensajes de comando al recuperar información del dispositivo.

Cuando se analizan los comandos, esta información general usa el formato de cadena del comando seguido del formulario de mensaje entre paréntesis.

 

 