---
description: Explica la arquitectura del sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Arquitectura del sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360227"
---
# <a name="cryptoapi-system-architecture"></a>Arquitectura del sistema CryptoAPI

La arquitectura del sistema CryptoAPI se compone de cinco áreas funcionales principales:

-   [Funciones criptográficas base](#base-cryptographic-functions)
-   [Funciones de codificación y descodificación de certificados](#certificate-encodedecode-functions)
-   [Funciones del almacén de certificados](#certificate-store-functions)
-   [Funciones de mensaje simplificadas](#simplified-message-functions)
-   [Funciones de mensajes de bajo nivel](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funciones criptográficas base

-   *Funciones de contexto* que se usan para conectarse a un CSP. Estas funciones permiten a las aplicaciones elegir un CSP específico por nombre o elegir un CSP específico que pueda proporcionar una clase de funcionalidad necesaria.
-   [*Funciones de generación de claves*](../secgloss/k-gly.md) usadas para generar y almacenar [*claves criptográficas*](../secgloss/c-gly.md). Se incluye compatibilidad completa para cambiar los [*modos de encadenamiento*](../secgloss/c-gly.md), los [*vectores de inicialización*](../secgloss/i-gly.md)y otras características de cifrado. Para obtener más información, consulte [generación de claves e intercambio de funciones](cryptography-functions.md).
-   *Funciones de intercambio de claves* que se usan para intercambiar o transmitir claves. Para obtener más información, consulte [almacenamiento de claves criptográficas y intercambio](cryptographic-key-storage-and-exchange.md) y [generación de claves y funciones de Exchange](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funciones de codificación y descodificación de certificados

-   Funciones utilizadas para cifrar o descifrar datos. También se incluye compatibilidad con los datos de [*hash*](../secgloss/h-gly.md) . Para obtener más información, vea [funciones de cifrado y descifrado de datos](cryptography-functions.md) y [cifrado y](data-encryption-and-decryption.md)descifrado de datos.

## <a name="certificate-store-functions"></a>Funciones del almacén de certificados

-   Funciones utilizadas para administrar recopilaciones de certificados digitales. Para obtener más información, vea [certificados digitales](digital-certificates.md) y [funciones del almacén de certificados](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funciones de mensaje simplificadas

-   Funciones utilizadas para cifrar y descifrar mensajes y datos.
-   Funciones utilizadas para firmar mensajes y datos.
-   Funciones que se usan para comprobar la autenticidad de las firmas en los mensajes recibidos y los datos relacionados.

Para obtener más información, vea [mensajes simplificados](simplified-messages.md) y [funciones de mensaje simplificadas](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Funciones de mensajes de bajo nivel

-   Funciones utilizadas para realizar todas las tareas realizadas por las funciones de mensaje simplificadas. Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificado, pero requieren más llamadas a funciones. Para obtener más información, vea [mensajes de bajo nivel](low-level-messages.md) y [funciones de mensajes de bajo nivel](cryptography-functions.md).

![arquitectura de CryptoAPI](images/cryparch.png)

Cada una de las áreas funcionales tiene una palabra clave en el nombre de función que indica su área funcional.



| Área funcional              | Convención de nombre de función |
|------------------------------|--------------------------|
| Funciones criptográficas base | Codifica                    |
| Funciones de codificación y descodificación  | Codifica                    |
| Funciones del almacén de certificados  | Tienda                    |
| Funciones de mensaje simplificadas | Message                  |
| Funciones de mensajes de bajo nivel  | Msg                      |



 

Las aplicaciones usan funciones en todas estas áreas. Estas funciones, tomadas juntas, componen CryptoAPI. Las [*funciones criptográficas base*](../secgloss/b-gly.md) usan los CSP para los algoritmos criptográficos necesarios y para la generación y el almacenamiento seguro de [claves criptográficas](cryptographic-keys.md).

Se usan dos tipos diferentes de claves criptográficas: [*las claves de sesión*](../secgloss/s-gly.md), que se usan para un solo cifrado y descifrado, y [*pares de claves pública y privada*](../secgloss/p-gly.md), que se usan de forma más permanente.

> [!Note]  
> Aunque una aplicación puede comunicarse directamente con cualquiera de las cinco áreas funcionales, no se puede comunicar directamente con un CSP. Todas las comunicaciones de aplicación a CSP se producen a través de las [*funciones criptográficas base*](../secgloss/b-gly.md). Las funciones criptográficas base tienen un parámetro que especifica el CSP que se va a usar. Este parámetro se puede establecer en **null** para seleccionar un CSP predeterminado.

 

 

 
