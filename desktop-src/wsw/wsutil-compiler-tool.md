---
title: Herramienta del compilador WsUtil
description: La herramienta compilador de servicios Web de Windows, WsUtil.exe, admite el modelo de servicio y la serialización de tipos de datos. Procesa WSDL, esquemas XML y documentos de Directiva, y genera encabezados y archivos de código fuente de C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servicios Web de la herramienta compilador de WsUtil para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995749"
---
# <a name="wsutil-compiler-tool"></a>Herramienta del compilador WsUtil

La herramienta compilador de servicios Web de Windows, WsUtil.exe, admite el [modelo de servicio](service-model-layer-overview.md) y la [serialización](serialization.md) de tipos de datos. Procesa WSDL, esquemas XML y documentos de Directiva, y genera encabezados y archivos de código fuente de C. Esta herramienta es similar a la herramienta de compilación WSDL para código administrado, pero está destinada a código nativo.

Para admitir el [modelo de servicio](service-model-layer-overview.md), WsUtil.exe genera encabezados que se usarán tanto para el cliente como para el servicio. Genera un archivo de proxy de C para el lado cliente y archivos de código auxiliar de C para el servicio, según sea necesario.

Para admitir la [serialización](serialization.md), el compilador genera encabezados para las descripciones de elementos de las definiciones de elementos globales y toda la información de definición de tipos en los archivos de proxy que usa el motor de serialización.


Para ver las opciones de línea de comandos para procesar archivos WSDL, archivos de esquema XML y archivos de directiva de servicio Web, vea los temas siguientes:

-   [Herramienta de compilador de servicio Web](web-service-compiler-tool.md)
-   [WSDL y contratos de servicio](wsdl-support.md)
-   [Compatibilidad con esquemas](schema-support.md)
-   [Compatibilidad con directivas](policy-support.md)

## <a name="security"></a>Seguridad

Cuando use WsUtil, tenga en cuenta los siguientes problemas y observe las precauciones adecuadas:

-   Wsutil no recupera metadatos XML a través de la red y Wsutil no resuelve instrucciones Import ni include en los archivos de metadatos de entrada. Wsutil abre y lee archivos WSDL, XSD y de directivas. Los metadatos XML no son resistentes contra alteraciones. Asegúrese de que solo se utilizan WSDL, XSD y archivos de directivas desde el origen de confianza y asegúrese de proteger los archivos contra la manipulación antes y después de usarlos. Revise cuidadosamente el contenido de los archivos de entrada y compruebe que el contenido de los archivos es seguro para su uso en la aplicación. Wsutil.exe no realiza ninguna comprobación de la autenticidad de los archivos de metadatos.
-   Wsutil genera archivos de encabezado y de código auxiliar, que no son resistentes contra alteraciones. Debe establecer los derechos de acceso de nivel correctos en los archivos de código fuente generados por wsutil.exe para impedir el acceso de unauthoritized a esos archivos. Wsutil usa System. IO. StreamWriter para crear los archivos de salida.
-   Los usuarios deben tener en cuenta que Wsutil puede sobrescribir sus archivos locales y deben tener cuidado de especificar nombres de archivo y directorios seguros para los archivos de salida mediante el modificador/out.
-   Wsutil o wsutilhelper.dll se cargan en wsutil.exe, pueden finalizar de forma inesperada o consumir una gran cantidad de recursos del sistema cuando están en ataque o en el procesamiento de una cantidad muy grande de metadatos de entrada. La herramienta está diseñada para usarse solo durante el desarrollo. esta herramienta solo se debe usar como herramienta de tiempo de desarrollo. Puede que no sea seguro usarlo en el nivel intermedio para procesar la información de la Directiva.
-   Wsutilhelper.dll archivo DLL de la aplicación auxiliar se carga en wsutil.exe administrados para procesar la información de la Directiva. El usuario debe asegurarse de que no existe ningún binario malintencionado con el mismo nombre de archivo en la ruta de acceso binaria. Del mismo modo, el usuario debe asegurarse de que en el entorno de compilación, la ruta de acceso binaria está configurada correctamente y que no existe ningún binario malintencionado con el mismo nombre de "wsutil.exe".
-   Wsutil genera una anotación SAL para las operaciones y los campos de estructura siempre que sea posible. El usuario de los archivos generados por wsutil debe seguir el requisito especificado a través de la anotación SAL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la capa de modelo de servicio](service-model-layer-overview.md)
</dt> <dt>

[Serialización](serialization.md)
</dt> <dt>

[Herramienta de compilador de servicio Web](web-service-compiler-tool.md)
</dt> <dt>

[Compatibilidad con WSDL](wsdl-support.md)
</dt> <dt>

[Compatibilidad con esquemas](schema-support.md)
</dt> <dt>

[Compatibilidad con directivas](policy-support.md)
</dt> </dl>

 

 




