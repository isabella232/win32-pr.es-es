---
description: Las funciones de mensaje de bajo nivel codifican datos para la transmisión y descodificación de datos que se han recibido. Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funciones de mensajes de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810249"
---
# <a name="low-level-message-functions"></a>Funciones de mensajes de bajo nivel

Las [*funciones de mensaje de bajo nivel*](../secgloss/l-gly.md) codifican datos para la transmisión y descodificación de datos que se han recibido. Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.

Cuando se abre un mensaje mediante una función de apertura de mensaje de bajo nivel, permanece abierto y disponible (mantiene su [*Estado*](../secgloss/s-gly.md)) hasta que se cierra. Esto permite que un mensaje se construya por etapas mediante varias llamadas a la función [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .

El uso de funciones de mensaje de bajo nivel requiere más llamadas a funciones que el uso de funciones de mensaje simplificadas (vea [mensajes simplificados](simplified-messages.md)). Si se usan las funciones de mensaje simplificado, se realiza más trabajo dentro de las funciones de la API.

El uso de funciones de mensaje de bajo nivel implica el trabajo adicional de realizar llamadas a otras funciones criptográficas o de certificado. Por ejemplo, es posible que se necesiten datos de llamadas a funciones de certificado para inicializar estructuras utilizadas por estas funciones de mensaje de bajo nivel. Las funciones de mensaje simplificadas inicializan muchas de estas estructuras internamente.

En la tabla siguiente se enumeran las secciones con descripciones de procedimientos y ejemplos de código de C del uso de las funciones de mensaje de bajo nivel.



| Sección                                                                               | Contenido                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Funciones de mensajes de bajo nivel](cryptography-functions.md) | Muestra las funciones de mensaje de bajo nivel.             |
| [Firmar datos](signing-data.md)                                                      | Detalla las tareas necesarias para firmar los datos.             |
| [Codificación de datos con doble cifrado](encoding-enveloped-data.md)                                | Detalla las tareas necesarias para codificar los datos con doble cifrado. |
| [Descodificar datos con doble cifrado](decoding-enveloped-data.md)                                | Detalla las tareas necesarias para descodificar los datos con doble cifrado. |



 

 

 
