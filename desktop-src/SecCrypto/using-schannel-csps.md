---
description: El motor de protocolo SSL (Schannel) utiliza un proveedor de servicios criptográficos (CSP) al realizar operaciones criptográficas. Las aplicaciones criptográficas pueden llamar a CryptAcquireContext mediante los proveedores de aprovisionamiento de aprovisionamiento de \_ RSA \_ Schannel y Prov \_ DH \_ .
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: Uso de CSP de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687074"
---
# <a name="using-schannel-csps"></a>Uso de CSP de Schannel

El motor de protocolo SSL ([*Schannel*](../secgloss/s-gly.md)) utiliza un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) al realizar operaciones criptográficas. Las aplicaciones criptográficas pueden llamar a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) mediante los proveedores de aprovisionamiento de aprovisionamiento de \_ RSA \_ Schannel y Prov \_ DH \_ .

En esta sección se definen los tipos de [*CSP*](../secgloss/c-gly.md) RSA y Diffie-Hellman Schannel y se describe la funcionalidad que un CSP debe admitir para ser compatible con Schannel.dll, el motor de protocolo criptográfico. Un motor de protocolo es un programa que establece un canal de comunicaciones seguro entre una aplicación de cliente y de servidor.

Las aplicaciones no deben intentar usar la información de esta documentación para usar el canal de aprovisionamiento de aprovisionamiento de aprovisionamiento de aprovisionamiento de \_ RSA \_ Schannel o Prov \_ DH \_ directamente. En su lugar, en esta documentación se explica cómo los desarrolladores y proveedores de CSP deben escribir los CSP Schannel que son compatibles con los proveedores de Microsoft Schannel.

Esta documentación está pensada para ayudar a los desarrolladores de CSP a implementar CSP compatibles con RSA o Diffie-Hellman Schannel. Se supone que los desarrolladores están familiarizados con la versión 3,0 del Protocolo de [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL), la criptografía de [*clave pública*](../secgloss/p-gly.md) , los [*certificados digitales*](../secgloss/d-gly.md)y el conjunto de funciones de CryptoAPI. A los desarrolladores nuevos en estos temas se les aconseja leer la especificación del protocolo SSL 3,0 y la documentación de [Cryptography Essentials](cryptography-essentials.md) en este SDK. Además, los desarrolladores de RSA y Diffie-Hellman CSP deben conocer las especificaciones del Protocolo de seguridad de la [*capa de transporte*](../secgloss/t-gly.md) (TLS) junto con los algoritmos de RSA y [*Diffie-Hellman*](../secgloss/d-gly.md)correspondientes.

Para obtener un ejemplo utilizado por un motor de protocolo de Microsoft, vea [crear la clave maestra](creating-the-master-key.md). Las llamadas a las funciones de criptografía en este ejemplo dan como resultado llamadas a funciones de CP que un CSP debe implementar. Para escribir un CSP compatible, un desarrollador debe comprender la especificación SSL 3,0 y combinar dicho conocimiento con una comprensión del código del motor de protocolo similar al que se usa en este ejemplo.

Dado que se espera que el uso del Protocolo de tecnología de comunicaciones privadas sea mínimo en el futuro, no es necesario que los desarrolladores de nuevos CSP admitan este protocolo. El motor de protocolo Schannel lo admite estrictamente para la compatibilidad con versiones anteriores.

 

 
