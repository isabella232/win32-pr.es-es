---
description: Las claves criptográficas son esenciales para las operaciones criptográficas.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Claves criptográficas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82858b26fa70ceacb4e7f9714e29983a773e66ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497218"
---
# <a name="cryptographic-keys"></a>Claves criptográficas

[*Las claves criptográficas*](../secgloss/c-gly.md) son esenciales para las operaciones criptográficas. Muchos esquemas criptográficos están compuestos por pares de operaciones, como el cifrado y el descifrado, o la firma y comprobación. Una *clave* es un fragmento de datos variables que se introduce como entrada en un algoritmo criptográfico para realizar una operación de este tipo. En un esquema criptográfico bien diseñado, la seguridad del esquema depende solo de la seguridad de las claves utilizadas.

Las claves criptográficas se pueden clasificar en función de su uso dentro de un esquema criptográfico, como [claves simétricas](symmetric-keys.md) o [claves asimétricas](public-private-key-pairs.md). Una [*clave simétrica*](../secgloss/s-gly.md) es una clave única que se usa para ambas operaciones en un esquema criptográfico (por ejemplo, para [*cifrar*](../secgloss/e-gly.md) y [*descifrar*](../secgloss/d-gly.md) los datos). Normalmente, la seguridad del esquema depende de asegurarse de que solo los participantes autorizados conocen la clave. Por otro lado, las claves asimétricas se utilizan en esquemas criptográficos en los que se necesitan claves diferentes para cada operación. Algunos ejemplos comunes de estos esquemas son aquellos que usan [*pares de claves pública y privada*](../secgloss/p-gly.md), en los que la seguridad del esquema depende de asegurarse de que la [*clave privada*](../secgloss/p-gly.md) solo la conoce una entidad. Por ejemplo, los sistemas de cifrado de clave pública y privada utilizan dos claves, una [*clave pública*](../secgloss/p-gly.md) que cualquiera puede usar para cifrar datos y una [*clave privada*](../secgloss/p-gly.md) que solo posee el destinatario autorizado y que se puede usar para descifrar los datos.

Las claves criptográficas se pueden clasificar más por el propósito para el que se usan. Estos usos incluyen la generación de firmas digitales, la comprobación de la firma digital, la autenticación de mensajes, el cifrado y descifrado de datos, el encapsulado de claves y el transporte de claves. Para obtener una lista completa de los tipos de clave definidos por el [*Instituto Nacional de estándares y Tecnología*](../secgloss/n-gly.md) (NIST), consulte la sección 5 guía general de administración de claves de la [publicación especial de NIST 800-57: Recomendación para la administración de claves, parte 1: General (revisado)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
