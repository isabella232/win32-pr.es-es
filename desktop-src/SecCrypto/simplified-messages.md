---
description: Se ha proporcionado un grupo de funciones de alto nivel para simplificar y reducir la cantidad de código necesario para realizar las tareas habituales de manipulación de mensajes.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Mensajes simplificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173101"
---
# <a name="simplified-messages"></a>Mensajes simplificados

Se ha proporcionado un grupo de funciones de alto nivel para simplificar y reducir la cantidad de código necesario para realizar las tareas habituales de manipulación de mensajes. Estas funciones se denominan "funciones de mensaje simplificadas". Los nombres de todas las funciones de mensaje simplificadas contienen la palabra "Mensaje".

[*Las funciones de mensaje*](../secgloss/s-gly.md) simplificadas están en un nivel mayor que las funciones criptográficas base o las funciones de mensaje de bajo nivel. Encapsulan varias de las funciones criptográficas, de bajo nivel y de certificado base en una sola función que realiza una tarea específica de una manera específica, como cifrar un mensaje PKCS 7 o firmar un \# mensaje. Las funciones de mensaje simplificadas proporcionan una manera rápida de empezar a usar CryptoAPI mediante la reducción del número de llamadas de función necesarias para realizar una tarea.

En la tabla siguiente se muestran las secciones que contienen descripciones detalladas de procedimientos o ejemplos del programa C sobre el uso de las funciones de mensaje simplificadas.



| Sección                                                                                                                                         | Contenido                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Funciones de mensaje simplificadas](cryptography-functions.md)                                                         | Enumera las funciones de mensaje simplificadas.                                                     |
| [Crear un mensaje firmado](creating-a-signed-message.md)                                                                                      | Detalla el proceso de creación de un mensaje firmado.                                           |
| [Procedimiento para firmar datos](procedure-for-signing-data.md)                                                                                    | Proporciona un procedimiento para usar las funciones de mensaje simplificadas para crear un mensaje firmado. |
| [Comprobación de un mensaje firmado](verifying-a-signed-message.md)                                                                                    | Detalla un proceso para comprobar la firma en un mensaje firmado.                          |
| [Cifrado de un mensaje](../secauthn/encrypting-a-message.md)                                                                                           | Detalla las tareas necesarias para cifrar y descifrar un mensaje.                                  |
| [Descifrar un mensaje](../secauthn/decrypting-a-message.md)                                                                                           | Detalla las tareas necesarias para descifrar un mensaje.                                              |
| [Programa de C de ejemplo: uso de CryptEncryptMessage y CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Proporciona un procedimiento y código de ejemplo para cifrar y descifrar un mensaje.               |



 

 

 
