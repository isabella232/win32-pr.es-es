---
title: Lenguaje de definición de interfaz de Microsoft
description: El Lenguaje de definición de interfaz de Microsoft (MIDL) define interfaces entre los programas cliente y servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL , (vea Lenguaje de definición de interfaz de Microsoft MIDL )
- Lenguaje de definición de interfaz de Microsoft MIDL
- Lenguaje de definición de interfaz de Microsoft MIDL, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9062d5b2af18f7c3aa5ad57a4cb8f606cccc43333e4eff17d3518f72b7a064a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534975"
---
# <a name="microsoft-interface-definition-language"></a>Lenguaje de definición de interfaz de Microsoft

## <a name="purpose"></a>Propósito

El Lenguaje de definición de interfaz de Microsoft (MIDL) define interfaces entre los programas cliente y servidor. Microsoft incluye el compilador MIDL con el Kit de desarrollo de software de plataforma (SDK) para permitir a los desarrolladores crear los archivos del lenguaje de definición de interfaz (IDL) y los archivos de configuración de aplicaciones (ACF) necesarios para las interfaces de llamada a procedimiento remoto (RPC) y las interfaces COM/DCOM. MIDL también admite la generación de bibliotecas de tipos para OLE Automation.

## <a name="where-applicable"></a>Donde sea aplicable

MIDL se puede usar en todas las aplicaciones cliente/servidor basadas en Windows sistemas operativos. También se puede usar para crear programas de cliente y servidor para entornos de red heterogéneos que incluyen sistemas operativos como Unix y Apple. Microsoft admite el estándar DCE open group (anteriormente conocido como Open Software Foundation) para la interoperabilidad rpc.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Al usar MIDL con RPC, es necesario estar familiarizado con la programación de C/C++ y el paradigma RPC. Cuando se usa MIDL con COM, es necesario estar familiarizado con la programación de C++ y el paradigma RPC cuando se aplica a COM, o bien, es necesario estar familiarizado con el scripting del modelo ole Automation y las bibliotecas de tipos.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las bibliotecas en tiempo de ejecución adecuadas para usar MIDL se incluyen con Windows. El compilador MIDL y los componentes del entorno de desarrollo rpc se instalan al instalar el SDK Windows. Para obtener más información, vea [Usar el compilador MIDL](using-the-midl-compiler-2.md) e [Instalar el entorno de programación RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                               | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Información general](about-this-guide-2.md)<br/>                                                       | Información general sobre MIDL y el compilador midl.<br/>                   |
| [Uso del compilador midl](using-the-midl-compiler-2.md)<br/>                                 | Información sobre el uso del compilador MIDL para generar código auxiliar RPC.<br/>       |
| [Definiciones de interfaz y bibliotecas de tipos](interface-definitions-and-type-libraries.md)<br/> | Documentación de definiciones de interfaz específicas de RPC y bibliotecas de tipos.<br/> |
| [Referencia de Command-Line MIDL](midl-command-line-reference.md)<br/>                           | Documentación de los modificadores de línea de comandos del compilador MIDL.<br/>               |
| [Referencia del lenguaje MIDL](midl-language-reference.md)<br/>                                   | Referencia del lenguaje del compilador MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamada a procedimiento remoto (RPC)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

