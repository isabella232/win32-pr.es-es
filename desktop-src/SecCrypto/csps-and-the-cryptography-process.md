---
description: Las funciones cryptoAPI usan proveedores de servicios criptográficos (CSP) para realizar el cifrado y descifrado, y para proporcionar seguridad y almacenamiento de claves.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSP y el proceso de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc1813f5f4bff96470c23ff8e777ef15458bddf7773663b4d16d9618e371a15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100935"
---
# <a name="csps-and-the-cryptography-process"></a>CSP y el proceso de criptografía

[*Las funciones cryptoAPI*](../secgloss/c-gly.md) usan [*proveedores de*](../secgloss/c-gly.md) servicios criptográficos (CSP) para realizar el cifrado y descifrado, y para proporcionar seguridad y almacenamiento de claves. Estos CSP son módulos independientes. Idealmente, los CSP se escriben para que sean independientes de una aplicación determinada, por lo que cualquier aplicación se ejecutará con una variedad de CSP. En realidad, sin embargo, algunas aplicaciones tienen requisitos específicos que requieren un CSP personalizado. Esto se compara con el modelo Windows [*GDI.*](../secgloss/g-gly.md) Los CSP son análogos a los controladores de dispositivos gráficos.

La calidad de protección de las claves dentro del sistema es un parámetro de diseño del CSP y no del sistema en su conjunto. Esto permite que una aplicación se ejecute en diversos contextos de seguridad sin modificaciones.

Las aplicaciones de acceso a los recursos internos criptográficos están cuidadosamente restringidas. Esto facilita el desarrollo de aplicaciones seguras y portátiles.

Se aplican las tres reglas de diseño siguientes:

-   Las aplicaciones no pueden acceder directamente al material de claves. Dado que todo el material de clave se genera dentro del CSP y lo usa la aplicación a través de controladores opacos, no hay ningún riesgo de que una aplicación o sus archivos DLL asociados divulgen material de clave o elijan material de clave de orígenes aleatorios deficientes.
-   Las aplicaciones no pueden especificar los detalles de las operaciones criptográficas. La interfaz CSP permite que una aplicación elija un algoritmo de cifrado o firma, pero la implementación de cada operación criptográfica la realiza el CSP.
-   Las aplicaciones no controlan las credenciales de [*usuario ni*](../secgloss/c-gly.md) otros datos de autenticación de usuario. El CSP realiza la autenticación de usuario; Por lo tanto, los FUTUROS con funcionalidades de autenticación avanzadas, como las entradas biométricas, funcionarán sin necesidad de cambiar el modelo de autenticación de aplicaciones.

Como mínimo, un CSP consta de una biblioteca de vínculos dinámicos (DLL) y un archivo [*de firma*](../secgloss/s-gly.md). El archivo de firma es necesario para asegurarse de que [*CryptoAPI*](../secgloss/c-gly.md) reconoce el CSP. CryptoAPI valida esta firma periódicamente para asegurarse de que se detecta cualquier manipulación con el CSP.

Algunos CSP pueden implementar una fracción de su funcionalidad en un servicio separado por direcciones llamado a través de RPC local o en hardware llamado a través de un controlador de dispositivo del sistema. Aislar las operaciones criptográficas centrales y de estado de clave globales en un servicio separado por direcciones o en hardware evita que las claves y las operaciones se manipule dentro de un espacio de datos de la aplicación.

No es imprudente que las aplicaciones aprovechen los atributos específicos de un CSP específico. Por ejemplo, el proveedor criptográfico base de Microsoft (proporcionado con CryptoAPI) admite claves de sesión de 40 bits y claves públicas de 512 bits. Las aplicaciones que manipulan estas claves deben evitar suposiciones sobre la cantidad de memoria necesaria para almacenar estas claves, ya que es probable que la aplicación no se pueda usar si se usa un CSP diferente. Las aplicaciones bien escritas deben funcionar con una variedad de CSP.

Para obtener más información sobre los tipos de proveedor de servicios criptográficos y los PROVEEDORES de servicios criptográficos predefinidos que se pueden usar con CryptoAPI, vea [Tipos](cryptographic-provider-types.md) de proveedor de servicios criptográficos y Proveedores de [servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md).

 

 
