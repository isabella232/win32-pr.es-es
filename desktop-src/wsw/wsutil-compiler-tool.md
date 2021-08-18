---
title: Herramienta WsUtil Compiler
description: La Windows compilador de servicios web, WsUtil.exe, admite el modelo de servicio y la serialización de tipos de datos. Procesa documentos WSDL, esquemas XML y directivas, y genera encabezados Y archivos de código fuente de C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servicios web de la herramienta WsUtil Compiler para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9a4e5761a068e991463451595c410c01f868d4d3e6c9df6ab25a7cb232d678
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119324905"
---
# <a name="wsutil-compiler-tool"></a>Herramienta WsUtil Compiler

La Windows compilador de servicios web, WsUtil.exe, admite [](service-model-layer-overview.md) el modelo de servicio y [la serialización](serialization.md) de tipos de datos. Procesa documentos WSDL, esquemas XML y directivas, y genera encabezados Y archivos de código fuente de C. Esta herramienta es similar a la herramienta del compilador WSDL para código administrado, pero está dirigida al código nativo en su lugar.

Para admitir el [modelo de servicio](service-model-layer-overview.md), WsUtil.exe genera encabezados que se usarán para el cliente y el servicio. Genera el archivo proxy de C para el lado cliente y los archivos de código auxiliar de C para el lado del servicio, según sea necesario.

Para [admitir](serialization.md)la serialización , el compilador genera encabezados para descripciones de elementos para definiciones de elementos globales y toda la información de definición de tipos en los archivos proxy que consume el motor de serialización.


Para obtener opciones de línea de comandos para procesar archivos WSDL, archivos de esquema XML y archivos de directiva de servicio web, vea los temas siguientes:

-   [Herramienta del compilador de servicios web](web-service-compiler-tool.md)
-   [WSDL y contratos de servicio](wsdl-support.md)
-   [Compatibilidad con esquemas](schema-support.md)
-   [Compatibilidad con directivas](policy-support.md)

## <a name="security"></a>Seguridad

Cuando use WsUtil, tenga en cuenta los siguientes problemas y observe las precauciones adecuadas:

-   Wsutil no recupera metadatos XML a través de la red y wsutil no resuelve las instrucciones import o include en los archivos de metadatos de entrada. Wsutil abre y lee archivos wsdl, xsd y de directiva. Los metadatos XML no son resistentes a alteraciones. Asegúrese de que solo se usan archivos wsdl, xsd y de directiva de origen de confianza y asegúrese de proteger los archivos de la manipulación antes y después de usarlos. Revise cuidadosamente el contenido de los archivos de entrada y compruebe que el contenido de los archivos es seguro para su uso en la aplicación. Wsutil.exe no realiza ninguna comprobación de la autenticidad de los archivos de metadatos.
-   Wsutil genera archivos de encabezado y código auxiliar, que no son resistentes a alteraciones. Debe establecer los derechos de acceso de nivel correctos en los archivos de origen generados por wsutil.exe para evitar el acceso no autenticado a esos archivos. Wsutil usa System.IO.StreamWriter para crear los archivos de salida.
-   Los usuarios deben tener en cuenta que Wsutil puede sobrescribir sus archivos locales y deben tener cuidado de especificar directorios y nombres de archivo seguros para los archivos de salida mediante el modificador /out.
-   Wsutil o wsutilhelper.dll cargados en wsutil.exe, pueden finalizar inesperadamente o consumir una gran cantidad de recursos del sistema cuando se están bajo ataque o al procesar una gran cantidad de metadatos de entrada. La herramienta está diseñada para usarse solo durante el tiempo de desarrollo. Esta herramienta solo debe usarse como herramienta de tiempo de desarrollo. Es posible que no sea seguro usarlo en el nivel intermedio para procesar la información de la directiva.
-   Wsutilhelper.dll dll auxiliar se carga en la biblioteca wsutil.exe para procesar la información de la directiva. El usuario debe asegurarse de que no existe ningún archivo binario malintencionado con el mismo nombre de archivo en la ruta de acceso binaria. Del mismo modo, el usuario debe asegurarse de que, en el entorno de compilación, la ruta de acceso binaria se configura correctamente y que no existe ningún archivo binario malintencionado con el mismo nombre wsutil.exe".
-   Wsutil genera una anotación SAL para operaciones y campos de estructura cuando es posible. El usuario de los archivos generados por wsutil debe seguir el requisito especificado a través de la anotación SAL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la capa de modelo de servicio](service-model-layer-overview.md)
</dt> <dt>

[Serialización](serialization.md)
</dt> <dt>

[Herramienta del compilador de servicios web](web-service-compiler-tool.md)
</dt> <dt>

[Compatibilidad con WSDL](wsdl-support.md)
</dt> <dt>

[Compatibilidad con esquemas](schema-support.md)
</dt> <dt>

[Compatibilidad con directivas](policy-support.md)
</dt> </dl>

 

 




