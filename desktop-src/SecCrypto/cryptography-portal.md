---
description: Use tecnologías criptográficas para el cifrado de claves públicas, algoritmos de cifrado, cifrado RSA y certificados digitales.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050f84d118cb5ad9e1da49ddabd73489745339bb0b1357e229b0f1609a1c997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876115"
---
# <a name="cryptography"></a>Criptografía

## <a name="purpose"></a>Propósito

La criptografía es el uso de códigos para convertir datos para que solo un destinatario específico pueda leerlo, mediante una clave.

Las tecnologías criptográficas de Microsoft incluyen CryptoAPI, proveedores de servicios criptográficos (CSP), herramientas de CryptoAPI, CAPICOM, WinTrust, emisión y administración de certificados, y el desarrollo de infraestructuras de clave pública personalizables. También se describen la inscripción de certificados y tarjetas inteligentes, la administración de certificados y el desarrollo de módulos personalizados.

## <a name="developer-audience"></a>Audiencia de desarrolladores

CryptoAPI está pensado para que lo usen los desarrolladores de aplicaciones basadas en Windows que permitirán a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente a través de medios no seguros como Internet. Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++ y el Windows de programación. Aunque no es necesario, se recomienda comprender la criptografía o los temas relacionados con la seguridad.

CAPICOM es un componente de solo 32 bits destinado a desarrolladores que crean aplicaciones mediante el lenguaje de programación Visual Basic Scripting Edition (VBScript) o el lenguaje de programación C++. CAPICOM está disponible para su uso en los sistemas operativos especificados en Run-Time requisitos. Para el desarrollo futuro, se recomienda usar el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

CAPICOM 2.1.0.2 se admite en los siguientes sistemas operativos y versiones:

-   Windows Server 2003
-   Windows XP

CAPICOM está disponible como un archivo redistribuible que se puede descargar de [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Servicios de certificados requiere las siguientes versiones de estos sistemas operativos:

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>En esta sección



| Tema                                                           | Descripción                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la criptografía](about-cryptography.md)<br/>         | Conceptos clave de criptografía y una vista de alto nivel de las tecnologías de criptografía de Microsoft.<br/>                                                                                                                           |
| [Uso de criptografía](using-cryptography.md)<br/>         | Procesos criptográficos, procedimientos y ejemplos extendidos de C y Visual Basic mediante funciones CryptoAPI y objetos CAPICOM.<br/>                                                                            |
| [Referencia de criptografía](cryptography-reference.md)<br/> | Descripciones detalladas de las funciones de criptografía, interfaces, objetos, estructuras y otros elementos de programación de Microsoft. Incluye descripciones de referencia de la API para trabajar con certificados digitales.<br/> |



 

 

 




