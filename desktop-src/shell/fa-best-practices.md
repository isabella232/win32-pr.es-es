---
description: La siguiente lista son prácticas recomendadas que debe usar al trabajar con asociaciones de archivo.
title: Prácticas recomendadas para asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541086"
---
# <a name="best-practices-for-file-associations"></a>Prácticas recomendadas para asociaciones de archivos

La siguiente lista son prácticas recomendadas que debe usar al trabajar con asociaciones de archivo.

-   [No copiar asociaciones de archivo del registro](#do-not-copy-file-associations-from-the-registry)
-   [Evite Hard-Coding rutas de acceso en el registro siempre que sea posible](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Ajustar siempre las cadenas de expansión entre comillas](#always-wrap-expanding-strings-in-quotation-marks)
-   [No confunda reproducción automática/Autorun con asociaciones de archivos](#do-not-confuse-autoplayautorun-with-file-associations)
-   [No confunda la base de datos MIME de Internet Explorer con asociaciones de archivos](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usar ProgID con formato y con control de versiones correctos](#use-properly-formed-and-versioned-progids)
-   [No usar extensiones de nombre de archivo cortas](#do-not-use-short-file-name-extensions)
-   [Registrar nuevos tipos de archivo en la base de datos MIME de IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Registrarse con el servicio Web de Windows para asociaciones de archivos](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Temas relacionados](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>No copiar asociaciones de archivo del registro

Se recomienda no copiar las asociaciones de archivo existentes del registro. A menudo, esto conduce a la propagación de asociaciones de archivo con un formato incorrecto. En su lugar, debe seguir los pasos descritos en el [escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evite Hard-Coding rutas de acceso en el registro siempre que sea posible

Del mismo modo que las rutas de acceso de código duro en los programas pueden causar problemas, las rutas de acceso de código duro en el registro también pueden provocar problemas. En su lugar, debe usar las cadenas de expansión del registro (REG \_ Expand \_ SZ) para proporcionar independencia de la ruta de acceso cuando corresponda. Por ejemplo, en lugar de usar este método:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

Debe usar este método:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Ajustar siempre las cadenas de expansión entre comillas

Expandir cadenas puede contener espacios cuando se expanden. Dado que los espacios suelen interpretarse como delimitadores de argumentos, causan problemas en determinadas circunstancias. Por ejemplo, un comando para invocar mi programa puede almacenarse en el registro como:

`%SYSTEMROOT%\MyProgram %1 %2`

Mi programa espera que %1 sea la ruta de acceso completa a un nombre de archivo y %2 es un modificador para indicar alguna acción. Si este comando se ejecuta con **los argumentos C: \\ archivos de programa \\ Mis documentos \\document.txt** y **/Print**, y suponiendo que la raíz de c: \\ WinNT, se expande a:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

En este caso, el programa interpreta que el primer argumento es C: \\ Program y el segundo argumento es files \\ My, que no es el comportamiento previsto. Los argumentos se interpretan correctamente, sin embargo, independientemente de si contienen espacios, si las cadenas de expansión se incluyen entre comillas de la manera siguiente:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>No confunda reproducción automática/Autorun con asociaciones de archivos

Las asociaciones de archivos son similares a la reproducción automática y la ejecución automática de algunas maneras. Sin embargo, la reproducción automática y la ejecución automática ofrecen instalaciones independientes y distintas de las proporcionadas por las asociaciones de archivo. Para obtener más información [, consulte crear una aplicación de CD-ROM habilitada para Autorun](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>No confunda la base de datos MIME de Internet Explorer con asociaciones de archivos

Las asociaciones de archivos son similares a la base de datos MIME de Windows Internet Explorer, en los tipos de archivo que pueden (y deberían) incluir una definición de tipo MIME. Sin embargo, la base de datos MIME de Internet Explorer es independiente y distinta de las asociaciones de archivo.

## <a name="use-properly-formed-and-versioned-progids"></a>Usar ProgID con formato y con control de versiones correctos

Utilice siempre los [ProgID con versión](fa-progids.md), incluso si solo hay una versión de ProgID. Los ProgID con versión ayudan a evitar conflictos de ProgID y sobrescrituras. También permiten que las distintas versiones de una aplicación coexistan.

## <a name="do-not-use-short-file-name-extensions"></a>No usar extensiones de nombre de archivo cortas

Las extensiones de nombre de archivo largas ofrecen las siguientes ventajas:

-   La longitud limitada de las extensiones cortas hace que sean propensos a *colisiones de extensión.* Se produce una colisión de extensión cuando se utiliza la misma extensión para clasificar varios tipos de archivo. El uso de extensiones largas reduce considerablemente las posibilidades de una colisión.
-   Los nombres de archivo cortos tienden a ser algo crípticos. Las extensiones largas suelen ser más significativas, ya que se puede insertar información adicional en la extensión.

Para obtener más información, vea [extensiones de nombre de archivo](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrar nuevos tipos de archivo en la base de datos MIME de IANA

La autoridad de asignación de números de Internet (IANA) mantiene una base de datos pública de tipos MIME registrados. Al definir un nuevo tipo de archivo público, se recomienda definir también un tipo MIME para el tipo de archivo y registrar este tipo con la IANA. El registro no tiene ningún costo.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Registrarse con el servicio Web de Windows para asociaciones de archivos

Los desarrolladores de aplicaciones pueden registrarse con el servicio Web de Windows que usan los usuarios para buscar aplicaciones que puedan funcionar en tipos de archivo específicos. El proceso de registro con el servicio Web se detalla en el [proceso de incorporación del sistema de Asociación de archivos de Windows](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



