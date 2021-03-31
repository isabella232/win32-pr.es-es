---
title: Lenguaje de definición de interfaz de Microsoft
description: El Lenguaje de definición de interfaz de Microsoft (MIDL) define las interfaces entre los programas de cliente y servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (vea Lenguaje de definición de interfaz de Microsoft MIDL)
- Lenguaje de definición de interfaz de Microsoft MIDL
- Lenguaje de definición de interfaz de Microsoft MIDL, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077649"
---
# <a name="microsoft-interface-definition-language"></a>Lenguaje de definición de interfaz de Microsoft

## <a name="purpose"></a>Propósito

El Lenguaje de definición de interfaz de Microsoft (MIDL) define las interfaces entre los programas de cliente y servidor. Microsoft incluye el compilador de MIDL con el kit de desarrollo de software (SDK) de la plataforma para que los desarrolladores puedan crear los archivos de lenguaje de definición de interfaz (IDL) y los archivos de configuración de la aplicación (ACF) necesarios para las interfaces de llamada a procedimiento remoto (RPC) y las interfaces COM/DCOM. MIDL también admite la generación de bibliotecas de tipos para la automatización OLE.

## <a name="where-applicable"></a>Donde sea aplicable

Se puede usar MIDL en todas las aplicaciones cliente/servidor basadas en los sistemas operativos Windows. También se puede usar para crear programas de cliente y servidor para entornos de red heterogéneos que incluyen sistemas operativos como UNIX y Apple. Microsoft admite el estándar DCE Open Group (anteriormente conocido como Open Software Foundation) para la interoperabilidad de RPC.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Al usar MIDL con RPC, es necesario estar familiarizado con la programación de C/C++ y el paradigma de RPC. Al usar MIDL con COM, es necesario estar familiarizado con la programación de C++ y el paradigma de RPC a medida que se aplica a COM, o, como alternativa, estar familiarizado con el scripting de modelo de automatización OLE y las bibliotecas de tipos.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las bibliotecas en tiempo de ejecución adecuadas para usar MIDL se incluyen con Windows. El compilador de MIDL y los componentes del entorno de desarrollo de RPC se instalan cuando se instala el Windows SDK. Para obtener más información, vea [usar el compilador MIDL](using-the-midl-compiler-2.md) e [instalar el entorno de programación RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Información general](about-this-guide-2.md)<br/>                                                       | Información general sobre MIDL y el compilador de MIDL.<br/>                   |
| [Usar el compilador MIDL](using-the-midl-compiler-2.md)<br/>                                 | Información sobre el uso del compilador del de MIDL para generar código auxiliar de RPC.<br/>       |
| [Definiciones de interfaz y bibliotecas de tipos](interface-definitions-and-type-libraries.md)<br/> | Documentación de definiciones de interfaz y bibliotecas de tipos específicas de RPC.<br/> |
| [Referencia de Command-Line de MIDL](midl-command-line-reference.md)<br/>                           | Documentación de los modificadores de la línea de comandos del compilador MIDL.<br/>               |
| [Referencia del lenguaje MIDL](midl-language-reference.md)<br/>                                   | Referencia del lenguaje del compilador de MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamada a procedimiento remoto (RPC)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

