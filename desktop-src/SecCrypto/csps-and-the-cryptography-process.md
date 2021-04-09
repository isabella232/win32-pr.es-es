---
description: Las funciones de CryptoAPI usan proveedores de servicios de cifrado (CSP) para realizar el cifrado y el descifrado, así como para proporcionar seguridad y almacenamiento de claves.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSP y el proceso de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5404fc3641a9a2c753158f5acb84850f3f0f29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082058"
---
# <a name="csps-and-the-cryptography-process"></a>CSP y el proceso de criptografía

Las funciones de [*CryptoAPI*](../secgloss/c-gly.md) usan [*proveedores de servicios de cifrado*](../secgloss/c-gly.md) (CSP) para realizar el cifrado y el descifrado, así como para proporcionar seguridad y almacenamiento de claves. Estos CSP son módulos independientes. Idealmente, los CSP se escriben para ser independientes de una aplicación determinada, de modo que cualquier aplicación se ejecute con una variedad de CSP. Sin embargo, en realidad, algunas aplicaciones tienen requisitos específicos que requieren un CSP personalizado. Se compara con el modelo de Windows [*GDI*](../secgloss/g-gly.md) . Los CSP son análogos a los controladores de dispositivos de gráficos.

La calidad de la protección de las claves dentro del sistema es un parámetro de diseño del CSP y no del sistema en su totalidad. Esto permite que una aplicación se ejecute en una variedad de contextos de seguridad sin modificaciones.

Las aplicaciones de acceso a las internamente criptográficas se restringen cuidadosamente. Esto facilita el desarrollo de aplicaciones seguras y portátiles.

Se aplican las tres reglas de diseño siguientes:

-   Las aplicaciones no pueden tener acceso directamente al material de creación de claves. Dado que todo el material de creación de claves se genera dentro del CSP y lo usa la aplicación a través de identificadores opacos, no hay ningún riesgo de que una aplicación o sus archivos dll asociados revelan el material de creación de claves o eligen material de clave de orígenes aleatorios deficientes.
-   Las aplicaciones no pueden especificar los detalles de las operaciones criptográficas. La interfaz de CSP permite a una aplicación elegir un algoritmo de cifrado o de firma, pero el CSP realiza la implementación de cada operación criptográfica.
-   Las aplicaciones no controlan [*las credenciales*](../secgloss/c-gly.md) de usuario ni otros datos de autenticación de usuario. El CSP realiza la autenticación del usuario; por lo tanto, los futuros CSP con capacidades de autenticación avanzadas, como las entradas biométricas, funcionarán sin necesidad de cambiar el modelo de autenticación de la aplicación.

Como mínimo, un CSP consta de una biblioteca de vínculos dinámicos (DLL) y un [*archivo de signatura*](../secgloss/s-gly.md). El archivo de signatura es necesario para asegurarse de que [*CryptoAPI*](../secgloss/c-gly.md) reconoce el CSP. CryptoAPI valida esta firma periódicamente para asegurarse de que se detecta cualquier alteración con el CSP.

Algunos CSP pueden implementar una fracción de su funcionalidad en un servicio separado por direcciones llamado a través de RPC local o en hardware llamado a través de un controlador de dispositivo del sistema. El aislamiento de operaciones de cifrado globales y de estado de clave global en un servicio separado por la dirección o en el hardware mantiene las claves y las operaciones seguras de la manipulación dentro de un espacio de datos de la aplicación.

No es aconsejable que las aplicaciones aprovechen los atributos específicos de un CSP específico. Por ejemplo, el proveedor de servicios criptográficos de base de Microsoft (proporcionado con CryptoAPI) admite claves de sesión de 40 bits y claves públicas de 512 bits. Las aplicaciones que manipulen estas claves deben evitar suposiciones sobre la cantidad de memoria necesaria para almacenar estas claves, ya que es probable que se produzca un error en la aplicación si se usa un CSP diferente. Las aplicaciones bien escritas deben trabajar con diversos CSP.

Para obtener más información sobre los tipos de proveedor de servicios criptográficos y los CSP predefinidos que se pueden usar con CryptoAPI, consulte tipos de proveedor de servicios [criptográficos](cryptographic-provider-types.md) y [proveedores de servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md).

 

 
