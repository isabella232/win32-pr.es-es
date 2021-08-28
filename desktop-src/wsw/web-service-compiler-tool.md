---
title: Herramienta del compilador de servicios web
description: Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se usará tanto en el lado cliente como en el del servicio. Genera el archivo proxy de C para el lado cliente y el archivo de código auxiliar de C para el lado del servicio, según sea necesario.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Web Service Compiler Tool Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6789b9e2b6e38d89e422adc363326656b8f693e2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880986"
---
# <a name="web-service-compiler-tool"></a>Herramienta del compilador de servicios web

Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se usará tanto en el lado cliente como en el del servicio. Genera el archivo proxy de C para el lado cliente y el archivo de código auxiliar de C para el lado del servicio, según sea necesario.


Para admitir la [serialización](serialization.md), el compilador genera encabezados para las descripciones de elementos para las definiciones de elementos globales y toda la información de definición de tipos en el archivo proxy que el motor de serialización va a consumir.

Uso

**WsUtil.exe \[ modificadores de línea de comandos \[ switch-options: \] \] &lt; filename&gt;**

modificadores de línea de comandos

Especifica WsUtil.exe del compilador. Los modificadores pueden aparecer en cualquier orden. Dash ('-') y la barra diagonal ('/') se tratan como iguales.

Lista de opciones de línea de comandos

-   @filename Especifica que el archivo de entrada debe tratarse como un archivo de respuesta. Esta opción se puede usar varias veces, en cualquier lugar de la lista de argumentos.
-   /wsdl: filename :<dirección URL opcional> especifica que el archivo de entrada &lt; &gt; debe \_ tratarse como un archivo wsdl. Se permiten varias entradas wsdl y se procesan todos los archivos wsdl especificados. La dirección \_ URL opcional especifica la ubicación desde la que se recuperaron los metadatos. Si no se \_ especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente. Consulte también Compatibilidad [con directivas](policy-support.md).
-   /xsd: &lt; filename Especifica que el nombre de archivo de entrada debe &gt; tratarse como un archivo de esquema. Se permiten varias entradas xsd y se procesan todos los archivos de esquema especificados.
-   /wsp: filename :<dirección URL opcional> especifica que el nombre de archivo de entrada &lt; &gt; debe \_ tratarse como metadatos de directiva. Se permiten varias entradas wsp y se procesan todos los archivos de directiva especificados. La dirección \_ URL opcional especifica la ubicación desde la que se recuperaron los metadatos. Si no se \_ especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente. Los archivos de directiva se omiten si se especifica la marca /nopolicy. Consulte también Compatibilidad [con directivas](policy-support.md).
-   /nopolicy Deshabilitar el procesamiento de directivas.
-   /out: &lt; dirname &gt; Especifica el nombre del directorio para los archivos de salida
-   /noclient No genere el código auxiliar del lado cliente.
-   /noservice No genere el código auxiliar del servicio.
-   /prefix: &lt; cadena &gt; Anteponer la cadena especificada a todos los identificadores generados.
-   /fullname Anteponer el nombre de archivo normalizado a los identificadores generados. De forma predeterminada, solo se usará el nombre especificado en el atributo "name" para generar identificadores para las descripciones relacionadas.
-   /string:<WS \_ STRING>\|<WCHAR> De forma predeterminada, wsutil genera WCHAR para el tipo \* \* xsd:string. La aplicación puede usar esta marca para sobrescribir ese comportamiento y genera WS \_ STRING para xsd:type en su lugar.
-   /help Mostrar mensaje de ayuda
-   /? Igual que /help
-   /W:x Opciones de control de errores. Podría ser W:0-W:4 \| WX
-   /nologo No generar información específica del compilador en la salida de la consola.
-   /nostamp No generar información específica del compilador en los archivos generados.

De forma predeterminada, el compilador genera los siguientes archivos para el archivo WSDL o WSDL devuelto desde el intercambio de metadatos:

-   Proxy de cliente ({inputfilename}.c)
-   Código auxiliar de servicio ({inputfilename}.c)
-   Archivo de encabezado ({inputfilename}.h)

    La raíz del nombre de archivo generado es el nombre del archivo de entrada. Las extensiones de archivo de entrada originales se conservan para evitar la colisión de nombres de archivo para los archivos generados. De forma predeterminada, los códigos auxiliares de cliente y servicio se generan en el mismo archivo, con código auxiliar de servicio generado después del código proxy.

    De forma predeterminada, el compilador genera los siguientes archivos para un archivo XSD para el esquema devuelto desde el intercambio de metadatos:

-   descripciones de serialización ({inputfilename}.c)
-   Archivo de encabezado ({inputfilename}.h)

    La raíz del nombre de archivo es el nombre del servicio.

Wsutil.exe genera una sección "stamp" al principio de todos los archivos generados, lo que indica la opción del compilador, la versión de la herramienta, la opción de línea de comandos aplicable, etc. Esta sección se puede desactivar mediante la opción /nostamp para evitar ruido con la comparación de los archivos generados.

Wsutil no admite la descarga de metadatos

El compilador de Wsutil solo funciona desde el archivo de metadatos local. La herramienta no admite la descarga de metadatos de la ejecución de servicios web. Los desarrolladores pueden usar otras herramientas de servicio web compatibles, como svcutil, para descargar metadatos en el equipo local, inspeccionar los archivos guardados y pasar esos archivos a wsutil.exe para su compilación.

Compatibilidad con varios archivos de entrada y salida

El esquema WSDL y XML permite incluir o importar definiciones de otros espacios de nombres especificados en otras ubicación o archivos. Wsutil admite varias entradas de esquema, wsdl o directiva y genera un conjunto de código auxiliar o encabezado para cada archivo de entrada. Wsutil no sigue las instrucciones include e import. En su lugar, la aplicación debe pasar archivos que contengan todos los espacios de nombres necesarios a wsutil para que la herramienta pueda resolver todas las dependencias durante la compilación.

**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**

wsutil genera tres conjuntos de archivos de salida:

-   stockquote.xsd.c stockquote.xsd.h
-   stockquote.wsdl.c stockquote.wsdl.h
-   stockquoteservice.wsdl.h stockquoteservices.wsdl.c

Formato del archivo de salida

Para cada archivo de salida, wsutil genera definiciones disponibles externamente en el archivo de encabezado. Aparte de las definiciones de estructura de C y los prototipos de función de código auxiliar, todas las demás definiciones relacionadas con los servicios web se encapsulan en una estructura global denominada con nombre de archivo normalizado.

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

Observe que no todos los campos se generan para la estructura global. Solo se genera un campo de nivel superior cuando se especifican las definiciones relacionadas en el archivo de entrada. Por ejemplo, no se generan campos de mensajes, operaciones y contratos para los archivos xsd.

Niveles de advertencia y nivel de error

De forma similar al compilador de C, WsUtil.exe admite cuatro niveles de advertencia y un nivel de error:

-   WsUtil.exe genera errores con errores irrecuperables, como un archivo wsdl no válido, opciones del compilador no válidas, etc.
-   WsUtil genera advertencias W1 con problemas recuperables graves. El compilador puede seguir, pero el usuario debe ser consciente del problema. Por ejemplo, se generará una advertencia W1 si hay atributos no admitidos, como algunas facetas de WSDL, en wsdl que no afectan a la generación de código.
-   WsUtil genera advertencias W2 con problemas menos graves. No hay ninguna pérdida de funcionalidad, pero es posible que el desarrollador de aplicaciones quiera saberlo. Al igual que los comportamientos que pueden ser diferentes de otras plataformas.
-   WsUtil genera advertencias W3 con un impacto mínimo en el código generado. Por ejemplo, wsutil.exe genera una advertencia W3 cuando la cadena normalizada es diferente de la cadena original.
-   La advertencia W4 es más como las advertencias "informativos" y el problema WsUtil W4 en casos como omitir el atributo de documentación en WSDL.
-   WX indica que el compilador trata la advertencia como un error. Por ejemplo, wsutil genera un error para todas las advertencias de W1 si se especifica /W:1 /WX.

/W:{N} especifica qué nivel de mensaje de advertencia se debe generar. /W:1 significa que se deben generar advertencias de nivel de advertencia 1 y que las advertencias del nivel de advertencia 2 y las siguientes deben enmascararse y no generarse mediante la herramienta.

## <a name="fullname"></a>/fullname

Esta opción indica que WsUtil.exe nombre completo de los identificadores para evitar una posible colisión de nombres. Por ejemplo, en example.xsd tenemos:

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

De forma WsUtil.exe genera:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Pero si se especifica la opción de línea de comandos /fullname, WsUtil.exe genera la siguiente definición de estructura en su lugar:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalización

La herramienta es neutral en el idioma y se puede localizar a distintos idiomas. Se pueden localizar todos los mensajes de error o la salida de la consola. Sin embargo, las opciones de línea de comandos permanecen en inglés.

## <a name="environment-variable"></a>Variable de entorno

WsUtil.exe no usa ninguna variable de entorno.

## <a name="platform-independent"></a>Independiente de la plataforma

Los archivos de salida WsUtil.exe son independientes de la plataforma. No se genera código dependiente de la arquitectura en el código auxiliar; el compilador de C se encarga de todo lo que sea específico de la arquitectura. El código auxiliar se puede usar en todas las plataformas que se admiten.

La descripción de wsutil.exe salida se puede encontrar en compatibilidad [con WSDL y](wsdl-support.md) en la parte compatibilidad con [esquemas.](schema-support.md)

 

 




