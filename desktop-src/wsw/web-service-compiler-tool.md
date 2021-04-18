---
title: Herramienta de compilador de servicio Web
description: Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se va a usar tanto en el cliente como en el servicio. Genera el archivo de proxy de C para el lado cliente y el archivo de código auxiliar de C para el servicio, según sea necesario.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Servicios Web de herramienta del compilador de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421650"
---
# <a name="web-service-compiler-tool"></a>Herramienta de compilador de servicio Web

Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se va a usar tanto en el cliente como en el servicio. Genera el archivo de proxy de C para el lado cliente y el archivo de código auxiliar de C para el servicio, según sea necesario.


Para admitir la [serialización](serialization.md), el compilador genera encabezados para las descripciones de elementos de las definiciones de elementos globales y toda la información de definición de tipos en el archivo de proxy que va a consumir el motor de serialización.

Uso

**Modificador de la línea de comandos deWsUtil.exe- \[ \[ opciones \] :\]<filename>**

modificadores de línea de comandos

Especifica WsUtil.exe opciones del compilador. Los modificadores pueden aparecer en cualquier orden. Los guiones ('-') y la barra diagonal ('/') se tratan como los mismos.

Lista de opciones de la línea de comandos

-   @filename Especifica que el archivo de entrada debe tratarse como un archivo de respuesta. Esta opción se puede usar varias veces en cualquier lugar de la lista de argumentos.
-   /WSDL: <filename> : <\_ dirección url opcional> especifica que el archivo de entrada debe tratarse como un archivo WSDL. Se permiten varias entradas de WSDL y se procesan todos los archivos WSDL especificados. La \_ dirección URL opcional especifica la ubicación desde la que se recuperaron los metadatos. Si no \_ se especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente. Vea también [compatibilidad con directivas](policy-support.md).
-   /xsd: <filename> especifica que el nombre de archivo de entrada debe tratarse como un archivo de esquema. Se permiten varias entradas XSD y se procesan todos los archivos de esquema especificados.
-   /WSP: <filename> : <\_ dirección url opcional> especifica que el nombre de archivo de entrada debe tratarse como metadatos de la Directiva. Se permiten varias entradas WSP y se procesan todos los archivos de directivas especificados. La \_ dirección URL opcional especifica la ubicación desde la que se recuperaron los metadatos. Si no \_ se especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente. Los archivos de Directiva se omiten si se especifica la marca/nopolicy. Vea también [compatibilidad con directivas](policy-support.md).
-   /nopolicy deshabilite el procesamiento de directivas.
-   /out: <dirname> especifica el nombre de directorio para los archivos de salida
-   /noclient no generan el código auxiliar del lado cliente.
-   /noservice no generan el código auxiliar del lado de servicio.
-   /prefix: <string> antepone la cadena especificada a todos los identificadores generados.
-   /FullName antepone el nombre de archivo normalizado a los identificadores generados. De forma predeterminada, solo se utilizará el nombre especificado en el atributo "Name" para generar identificadores para las descripciones relacionadas.
-   /String: <\_ cadena WS>\|<WCHAR \*> de forma predeterminada, wsutil genera WCHAR \* para el tipo xsd: String. La aplicación puede usar esta marca para sobrescribir ese comportamiento y genera una \_ cadena WS para xsd: Type en su lugar.
-   /Help Mostrar mensaje de ayuda
-   /? Igual que/Help
-   Opciones de control de errores/w: x. Puede ser W:0-W: 4 \| WX
-   /nologo no generar información específica del compilador en la salida de la consola.
-   /nostamp no generan información específica del compilador en los archivos generados.

De forma predeterminada, el compilador genera los siguientes archivos para el archivo WSDL o el WSDL que devuelve el intercambio de metadatos:

-   Proxy de cliente ({InputFilename}. c)
-   Código auxiliar de servicio ({InputFilename}. c)
-   Archivo de encabezado ({InputFilename}. h)

    La raíz del nombre de archivo generado es el nombre del archivo de entrada. Las extensiones de archivo de entrada originales se conservan para evitar la colisión de nombres de archivo para los archivos generados. De forma predeterminada, los códigos auxiliares de cliente y servicio se generan en el mismo archivo, con código auxiliar de servicio generado después del código de proxy.

    De forma predeterminada, el compilador genera los siguientes archivos para un archivo XSD para el esquema devuelto desde el intercambio de metadatos:

-   descripciones de serialización ({InputFilename}. c)
-   Archivo de encabezado ({InputFilename}. h)

    La raíz del nombre de archivo es el nombre del servicio.

Wsutil.exe genera una sección "Stamp" al principio de todos los archivos generados, lo que indica la opción del compilador, la versión de herramienta, la opción de línea de comandos aplicable, etc. Esta sección se puede desactivar mediante la opción/nostamp para evitar el ruido con la comparación de archivos generados.

Wsutil no admite la descarga de metadatos

El compilador Wsutil solo funciona desde un archivo de metadatos local. La herramienta no admite la descarga de metadatos de servicios web en ejecución. Los desarrolladores pueden usar otras herramientas de WebService compatibles, como SvcUtil, para descargar los metadatos en la máquina local, inspeccionar los archivos guardados y pasarlos a wsutil.exe para su compilación.

Compatibilidad con varios archivos de entrada y salida

WSDL y el esquema XML permiten incluir o importar definiciones de otros espacios de nombres especificados en otros archivos o ubicaciones. Wsutil admite varias entradas de esquema/WSDL/Directiva y genera un conjunto de código auxiliar/encabezado para cada archivo de entrada. Wsutil no sigue las instrucciones include e import. En su lugar, la aplicación debe pasar archivos que contengan todos los espacios de nombres necesarios a wsutil de modo que la herramienta pueda resolver todas las dependencias durante la compilación.

**WsUtil.exe/xsd: stockquote. xsd/WSDL: stockquote. wsdl/WSDL: stockquoteservice. wsdl**

wsutil genera tres conjuntos de archivos de salida:

-   stockquote. xsd. c stockquote. xsd. h
-   stockquote. wsdl. c stockquote. wsdl. h
-   stockquoteservice. wsdl. h stockquoteservices. wsdl. c

Formato del archivo de salida

Para cada archivo de salida, wsutil genera definiciones externamente disponibles en el archivo de encabezado. Aparte de las definiciones de la estructura de C y los prototipos de función de código auxiliar, todas las demás definiciones relacionadas con servicios web se encapsulan en una estructura global denominada con un nombre de archivo normalizado.

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

Tenga en cuenta que no todos los campos se generan para la estructura global. Solo se genera un campo de nivel superior cuando las definiciones relacionadas se especifican en el archivo de entrada. Por ejemplo, no se generan campos de mensajes, operaciones y contratos para los archivos xsd.

Niveles de advertencia y nivel de error

Del mismo modo que el compilador de C, WsUtil.exe admite cuatro niveles de advertencia y un nivel de error:

-   WsUtil.exe genera errores con errores irrecuperables, como un archivo WSDL no válido, opciones de compilador no válidas, etc.
-   WsUtil genera advertencias W1 con problemas recuperables graves. El compilador puede continuar, pero el usuario debe ser consciente del problema. Por ejemplo, se generará una advertencia W1 si hay atributos no compatibles, como algunas de las figuras de WSDL, en WSDL que no afecten a la generación de código.
-   WsUtil genera advertencias de W2 con problemas menos graves. No se pierde la funcionalidad, pero es posible que el desarrollador de aplicaciones desee saberlo. Como los comportamientos que pueden ser diferentes de otras plataformas.
-   WsUtil genera advertencias de W3 con un impacto mínimo en el código generado. Por ejemplo, wsutil.exe genera una advertencia de W3 cuando la cadena normalizada es diferente de la cadena original.
-   La advertencia de W4 es más similar a las advertencias "informativas" y WsUtil emite W4 en casos como omitir el atributo de documentación en WSDL.
-   WX indica que el compilador trata la advertencia como un error. Por ejemplo, wsutil genera un error para todas las advertencias de W1 si se especifica/W: 1/WX.

/W: {N} especifique el nivel de mensaje de advertencia que debe generarse. /W: 1 significa que se deben generar advertencias de nivel de ADVERTENCIA 1 y las advertencias del nivel de ADVERTENCIA 2 e inferior deben enmascararse y no generarse con la herramienta.

## <a name="fullname"></a>/fullname

Esta opción indica que WsUtil.exe genera un nombre completo para los identificadores con el fin de evitar posibles conflictos de nombres. Por ejemplo, en el ejemplo. xsd tenemos:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

De forma predeterminada WsUtil.exe genera:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Pero si se especifica la opción de línea de comandos/FullName, WsUtil.exe genera en su lugar la siguiente definición de estructura:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalización

La herramienta es independiente del idioma y se puede localizar en distintos idiomas. Se pueden localizar todos los mensajes de error y la salida de la consola. Sin embargo, las opciones de la línea de comandos permanecen en inglés.

## <a name="environment-variable"></a>Variable de entorno

WsUtil.exe no usa ninguna variable de entorno.

## <a name="platform-independent"></a>Independiente de la plataforma

Los archivos de salida de WsUtil.exe son independientes de la plataforma. No se ha generado ningún código dependiente de la arquitectura en el código auxiliar; el compilador de C se ocupará de cualquier arquitectura específica. El código auxiliar se puede usar en todas las plataformas admitidas.

La descripción de la salida de wsutil.exe se puede encontrar en la parte compatibilidad de [WSDL](wsdl-support.md) y en el [esquema](schema-support.md) .

 

 




