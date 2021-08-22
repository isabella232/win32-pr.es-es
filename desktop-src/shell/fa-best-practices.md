---
description: En la lista siguiente se recomiendan los procedimientos recomendados que debe usar al trabajar con asociaciones de archivos.
title: Procedimientos recomendados para asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094220"
---
# <a name="best-practices-for-file-associations"></a>Procedimientos recomendados para asociaciones de archivos

En la lista siguiente se recomiendan los procedimientos recomendados que debe usar al trabajar con asociaciones de archivos.

-   [No copiar asociaciones de archivo desde el Registro](#do-not-copy-file-associations-from-the-registry)
-   [Evite Hard-Coding rutas de acceso al Registro siempre que sea posible](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Ajustar siempre las cadenas expandiendo entre comillas](#always-wrap-expanding-strings-in-quotation-marks)
-   [No confundir la reproducción automática o la ejecución automática con asociaciones de archivo](#do-not-confuse-autoplayautorun-with-file-associations)
-   [No confundir la base de Internet Explorer MIME con asociaciones de archivo](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usar progID con el correcto y con control de versiones](#use-properly-formed-and-versioned-progids)
-   [No usar extensiones de nombre de archivo corto](#do-not-use-short-file-name-extensions)
-   [Registrar nuevos tipos de archivo en la base de datos MIME de IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Registrarse con el servicio Windows web para asociaciones de archivos](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Temas relacionados](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>No copiar asociaciones de archivo desde el Registro

Se recomienda no copiar las asociaciones de archivo existentes del Registro. Esto suele dar lugar a la propagación de asociaciones de archivos con un formato deficiente. En su lugar, debe seguir los pasos descritos en Escenario [de ejemplo de asociación de archivos](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evite Hard-Coding rutas de acceso al Registro siempre que sea posible

Del mismo modo que las rutas de acceso de codificación rígida en los programas pueden causar problemas, las rutas de acceso codificadas de forma rígida en el registro también pueden provocar problemas. En su lugar, debe usar cadenas de expansión del Registro (REG EXPAND SZ) para proporcionar independencia de ruta \_ de acceso cuando \_ corresponda. Por ejemplo, en lugar de usar este método:

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

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Ajustar siempre las cadenas expandiendo entre comillas

Las cadenas de expansión pueden contener espacios cuando se expanden. Dado que los espacios a menudo se interpretan como delimitadores de argumentos, provocan problemas en determinadas circunstancias. Por ejemplo, un comando para invocar MyProgram se puede almacenar en el registro como:

`%SYSTEMROOT%\MyProgram %1 %2`

MyProgram espera que %1 sea la ruta de acceso completa a un nombre de archivo y %2 es un modificador para indicar alguna acción. Si este comando se ejecuta con argumentos C: Archivos de **\\ programa Mis documentos \\ \\document.txt** **y /print**, y suponiendo un SYSTEMROOT de C: WINNT, se expande \\ a:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

En este caso, MyProgram interpreta que el primer argumento es C: Program y el segundo argumento es Files My, que no es \\ \\ el comportamiento previsto. Sin embargo, los argumentos se interpretan correctamente, independientemente de si contienen espacios, si las cadenas de expansión se encapsulan entre comillas como se indica a continuación:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>No confundir la reproducción automática o la ejecución automática con asociaciones de archivo

Las asociaciones de archivo son similares a la reproducción automática o la ejecución automática de algunas maneras. Sin embargo, reproducción automática/ejecución automática ofrece instalaciones independientes y distintas de las proporcionadas por las asociaciones de archivos. Para obtener más información, [consulte Creación de una aplicación de CD-ROM](autoplay.md)habilitada para ejecución automática.

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>No confundir la base de Internet Explorer MIME con asociaciones de archivo

Las asociaciones de archivo son similares a Windows Internet Explorer base de datos MIME, en que los tipos de archivo pueden (y deben) incluir una definición de tipo MIME. Sin embargo, Internet Explorer base de datos MIME es independiente y distinta de las asociaciones de archivos.

## <a name="use-properly-formed-and-versioned-progids"></a>Usar progID con el correcto y con control de versiones

Use siempre progID con [versiones,](fa-progids.md)incluso si solo hay una versión del ProgID. Los ProgID con versiones ayudan a evitar conflictos y sobrescrituras de ProgID. También permiten coexistir diferentes versiones de una aplicación.

## <a name="do-not-use-short-file-name-extensions"></a>No usar extensiones de nombre de archivo corto

Las extensiones de nombre de archivo largo ofrecen las siguientes ventajas:

-   La longitud limitada de las extensiones cortas las hace propensas a *colisiones de extensiones.* Se produce una colisión de extensiones cuando se usa la misma extensión para clasificar varios tipos de archivo. El uso de extensiones largas reduce significativamente las posibilidades de colisión.
-   Los nombres de archivo cortos tienden a ser algo crípticos. Las extensiones largas tienden a ser más significativas porque se puede incrustar información adicional en la extensión.

Para obtener más información, vea [Extensiones de nombre de archivo](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrar nuevos tipos de archivo en la base de datos MIME de IANA

Internet Assigned Numbers Authority (IANA) mantiene una base de datos pública de tipos MIME registrados. Al definir un nuevo tipo de archivo público, se recomienda definir también un tipo MIME para el tipo de archivo y registrar este tipo en IANA. El registro no tiene ningún costo.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Registrarse con el servicio Windows web para asociaciones de archivos

Los desarrolladores de aplicaciones pueden registrarse con el Windows web que usan los usuarios para buscar aplicaciones que puedan funcionar en tipos de archivo específicos. El proceso de registro con el servicio web se detalla en Windows de incorporación del sistema de asociación [de archivos](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenario de ejemplo de asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Establecer el acceso al programa y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



