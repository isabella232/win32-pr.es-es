---
description: Se ha proporcionado un grupo de funciones de alto nivel para simplificar y acortar la cantidad de código necesario para realizar las tareas habituales de manipulación de mensajes.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Mensajes simplificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154517"
---
# <a name="simplified-messages"></a>Mensajes simplificados

Se ha proporcionado un grupo de funciones de alto nivel para simplificar y acortar la cantidad de código necesario para realizar las tareas habituales de manipulación de mensajes. Estas funciones se denominan "funciones de mensaje simplificadas". Los nombres de todas las funciones de mensaje simplificadas contienen la palabra "mensaje".

[*Las funciones de mensaje simplificado*](../secgloss/s-gly.md) se encuentran en un nivel más alto que las funciones criptográficas base o las funciones de mensaje de bajo nivel. Encapsulan varias de las funciones criptográficas de nivel de datos y de cifrado básicas en una sola función que realiza una tarea específica de una forma específica, como el cifrado de un \# mensaje PKCS 7 o la firma de un mensaje. Las funciones de mensaje simplificado proporcionan una forma rápida de empezar a usar CryptoAPI reduciendo el número de llamadas a funciones necesarias para realizar una tarea.

En la tabla siguiente se enumeran las secciones que contienen descripciones de procedimientos detallados o ejemplos de programas de C del uso de las funciones de mensaje simplificadas.



| Sección                                                                                                                                         | Contenido                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Funciones de mensaje simplificadas](cryptography-functions.md)                                                         | Muestra las funciones de mensaje simplificadas.                                                     |
| [Crear un mensaje firmado](creating-a-signed-message.md)                                                                                      | Detalla el proceso de creación de un mensaje firmado.                                           |
| [Procedimiento para firmar datos](procedure-for-signing-data.md)                                                                                    | Proporciona un procedimiento para usar las funciones de mensaje simplificadas para crear un mensaje firmado. |
| [Comprobación de un mensaje firmado](verifying-a-signed-message.md)                                                                                    | Detalla un proceso para comprobar la firma de un mensaje firmado.                          |
| [Cifrado de un mensaje](../secauthn/encrypting-a-message.md)                                                                                           | Detalla las tareas necesarias para cifrar y descifrar un mensaje.                                  |
| [Descifrado de un mensaje](../secauthn/decrypting-a-message.md)                                                                                           | Detalla las tareas necesarias para descifrar un mensaje.                                              |
| [Programa C de ejemplo: uso de CryptEncryptMessage y CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Proporciona un procedimiento y código de ejemplo para cifrar y descifrar un mensaje.               |



 

 

 
