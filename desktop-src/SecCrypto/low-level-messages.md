---
description: Las funciones de mensaje de bajo nivel codifican los datos para la transmisión y descodificación de los datos recibidos. Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funciones de mensaje de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270940"
---
# <a name="low-level-message-functions"></a>Funciones de mensaje de bajo nivel

Las [*funciones de mensaje de bajo nivel*](../secgloss/l-gly.md) codifican los datos para la transmisión y descodificación de los datos recibidos. Las funciones de mensaje de bajo nivel también descifran y comprueban las firmas de los mensajes recibidos.

Cuando se abre un mensaje mediante una función abierta de mensaje de bajo nivel, permanece abierto y disponible (mantiene su estado [*)*](../secgloss/s-gly.md)hasta que se cierra. Esto permite que un mensaje se construya por fragmentos mediante varias llamadas a la [**función CryptMsgUpdate.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)

El uso de funciones de mensaje de bajo nivel requiere más llamadas de función que el uso de funciones de mensaje simplificadas (vea [Mensajes simplificados).](simplified-messages.md) Si se usan las funciones de mensaje simplificadas, se realiza más trabajo dentro de las funciones de la API.

El uso de funciones de mensaje de bajo nivel implica el trabajo adicional de realizar llamadas a otras funciones criptográficas o de certificado. Por ejemplo, es posible que se necesiten datos de llamadas a funciones de certificado para inicializar las estructuras usadas por estas funciones de mensaje de bajo nivel. Las funciones de mensaje simplificadas inicializan muchas de estas estructuras internamente.

En la tabla siguiente se enumeran secciones con descripciones de procedimientos y ejemplos de código C del uso de las funciones de mensaje de bajo nivel.



| Sección                                                                               | Contenido                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Funciones de mensaje de bajo nivel](cryptography-functions.md) | Enumera las funciones de mensaje de bajo nivel.             |
| [Firma de datos](signing-data.md)                                                      | Detalla las tareas necesarias para firmar los datos.             |
| [Codificación de datos con sobres](encoding-enveloped-data.md)                                | Detalla las tareas necesarias para codificar los datos sobreados. |
| [Decoding Enveloped Data](decoding-enveloped-data.md)                                | Detalla las tareas necesarias para descodificar los datos sobreados. |



 

 

 
