---
description: Explica la arquitectura del sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitectura del sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791ed0ebfc82df1dc7b6e9600d4e0455ae60df3da35cfe3f8fd613f7b230ebd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768816"
---
# <a name="cryptoapi-system-architecture"></a>Arquitectura del sistema CryptoAPI

La arquitectura del sistema CryptoAPI se compone de cinco áreas funcionales principales:

-   [Funciones criptográficas base](#base-cryptographic-functions)
-   [Funciones de codificación/descodificación de certificados](#certificate-encodedecode-functions)
-   [Funciones del almacén de certificados](#certificate-store-functions)
-   [Funciones de mensaje simplificadas](#simplified-message-functions)
-   [Funciones de mensaje de bajo nivel](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funciones criptográficas base

-   *Funciones de contexto* usadas para conectarse a un CSP. Estas funciones permiten a las aplicaciones elegir un CSP específico por nombre o elegir un CSP específico que pueda proporcionar una clase necesaria de funcionalidad.
-   [*Funciones de generación de*](../secgloss/k-gly.md) claves usadas para generar y almacenar [*claves criptográficas*](../secgloss/c-gly.md). Se incluye compatibilidad completa para cambiar los modos [*de encadenamiento,*](../secgloss/c-gly.md) [*los vectores de inicialización*](../secgloss/i-gly.md)y otras características de cifrado. Para obtener más información, vea [Key Generation and Exchange Functions](cryptography-functions.md).
-   *Funciones de intercambio de* claves usadas para intercambiar o transmitir claves. Para obtener más información, vea [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) y Key Generation and Exchange [Functions](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funciones de codificación/descodificación de certificados

-   Funciones usadas para cifrar o descifrar datos. También se incluye compatibilidad con los [*datos hash.*](../secgloss/h-gly.md) Para obtener más información, vea [Funciones de cifrado y descifrado de datos](cryptography-functions.md) y Cifrado y descifrado de [datos](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Funciones del almacén de certificados

-   Funciones que se usan para administrar colecciones de certificados digitales. Para obtener más información, [vea Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funciones de mensaje simplificadas

-   Funciones que se usan para cifrar y descifrar mensajes y datos.
-   Funciones que se usan para firmar mensajes y datos.
-   Funciones que se usan para comprobar la autenticidad de las firmas en los mensajes recibidos y los datos relacionados.

Para obtener más información, vea [Mensajes simplificados](simplified-messages.md) y [Funciones de mensaje simplificadas.](cryptography-functions.md)

## <a name="low-level-message-functions"></a>Funciones de mensaje de bajo nivel

-   Funciones que se usan para realizar todas las tareas realizadas por las funciones de mensaje simplificadas. Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificadas, pero requieren más llamadas de función. Para obtener más información, vea [Mensajes de bajo nivel](low-level-messages.md) y Funciones de mensaje de bajo [nivel](cryptography-functions.md).

![arquitectura cryptoapi](images/cryparch.png)

Cada una de las áreas funcionales tiene una palabra clave en su nombre de función que indica su área funcional.



| Área funcional              | Convención de nombre de función |
|------------------------------|--------------------------|
| Funciones criptográficas base | Cripta                    |
| Funciones de codificación y codificación  | Cripta                    |
| Funciones del almacén de certificados  | Tienda                    |
| Funciones de mensaje simplificadas | Message                  |
| Funciones de mensaje de bajo nivel  | Msg                      |



 

Las aplicaciones usan funciones en todas estas áreas. Estas funciones, realizadas juntas, son cryptoAPI. Las [*funciones criptográficas base*](../secgloss/b-gly.md) usan los CSP para los algoritmos criptográficos necesarios y para la generación y almacenamiento seguro de claves [criptográficas](cryptographic-keys.md).

Se usan dos tipos diferentes [](../secgloss/s-gly.md)de claves criptográficas: las claves de sesión , que se usan para un único cifrado y descifrado, y los pares de claves pública y privada [*,*](../secgloss/p-gly.md)que se usan de forma más permanente.

> [!Note]  
> Aunque una aplicación puede comunicarse directamente con cualquiera de las cinco áreas funcionales, no puede comunicarse directamente con un CSP. Todas las comunicaciones de aplicación a CSP se producen a través de las [*funciones criptográficas base*](../secgloss/b-gly.md). Las funciones criptográficas base tienen un parámetro que especifica qué CSP usar. Este parámetro se puede establecer en **NULL** para seleccionar un CSP predeterminado.

 

 

 
