---
description: En el ejemplo siguiente, una empresa hipotética de desarrollo de software denominada Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Ejemplo de Asociación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153621"
---
# <a name="file-association-example"></a>Ejemplo de Asociación de archivos

En el ejemplo siguiente, una empresa hipotética de desarrollo de software denominada Litware, Inc. crea un nuevo reproductor de audio llamado LitwarePlayer. Litware quiere diseñar una asociación de archivos entre LitwarePlayer y su tipo de archivo principal, que usa un formato de audio recién desarrollado que permite almacenar un CD de audio completo en menos de 10 kilobytes de memoria sin pérdida de calidad.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que las asociaciones de archivos predeterminadas funcionan en Windows 10. Para obtener más información, consulte la sección **cambios en la forma en que Windows 10 trata las aplicaciones predeterminadas** en [esta publicación](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Diseñar una nueva asociación de archivo

La empresa debe realizar los siguientes pasos.

1.  **Decida si el nuevo tipo de archivo se debe tratar como público o privado.** Este nuevo tipo de archivo es un tipo de medio. Dado que los usuarios intercambian archivos multimedia entre varias plataformas y puede haber otras aplicaciones que necesiten leer el formato LitwarePlayer, un tipo de archivo [público](fa-file-types.md) es el más apropiado.
2.  **Determine si este tipo de archivo ya está definido.** Compruebe la base de datos MIME de la autoridad de números asignados de Internet (IANA) y otras bases de datos de tipo de archivo público en Internet para determinar que no se ha definido ningún tipo de archivo comparable. Dado que se trata de un nuevo formato de archivo, debe definir un nuevo tipo de archivo.
3.  **Defina una extensión de nombre de archivo para el nuevo tipo de archivo.** Los desarrolladores eligen `.opa-ltw-audio` , que incorpora su abreviatura de proveedor y una sugerencia sobre lo que contiene el archivo. La investigación determina que nadie más usa la extensión. A continuación de las recomendaciones actuales, no se define ninguna extensión corta.
4.  **Defina un tipo MIME para el tipo de archivo y regístrelo con la IANA.** Litware define el nuevo tipo MIME como *audio/LitwarePlayer. 1* y prepara una aplicación de tipo MIME, siguiendo las instrucciones establecidas en los números de solicitud de comentarios (RFC) 2045, 2046, 2047 y 2048. A continuación, envían la aplicación a la IANA, que agrega el nuevo tipo de archivo a la base de datos de tipos MIME registrados.
5.  **Determine si existe un identificador de programa (ProgID) para el tipo de archivo.** Dado que se trata de un nuevo tipo de archivo, no existe ningún [ProgID](fa-progids.md) para él. Litware establece sobre el diseño de un nuevo ProgID para LitwarePlayer. Deciden el nombre descriptivo "LitwarePlayer audio Player" (que se almacena como un recurso en el archivo LitwarePlayer.exe) y diseñan un icono predeterminado que se usará para los archivos asociados a LitwarePlayer (también almacenados en LitwarePlayer.exe). Dado que LitwarePlayer es una nueva aplicación, se trata de un ProgID de versión 1.
6.  **Registre el identificador de programa.** Cuando se instala LitwarePlayer, el programa de instalación crea la siguiente entrada [ProgID](fa-progids.md) en el registro.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    En la clave de comando, se pasa %1 como ruta de acceso al archivo que se va a reproducir.

7.  **Registra la extensión de nombre de archivo para el tipo de archivo.** Cuando se instala LitwarePlayer, el programa de instalación crea las siguientes entradas en el registro para su extensión de tipo de archivo personalizado.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Siempre que se crea o se cambia una asociación de archivo, notifique al sistema que se ha realizado un cambio llamando a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el \_ evento ASSOCCHANGED de SHCNE. Si no se hace esto, es posible que el shell no reconozca los cambios realizados hasta que se reinicie el sistema.

 

## <a name="additional-resources"></a>Recursos adicionales

-   [Introducción a las asociaciones de archivos](fa-intro.md)
-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
-   [Registrar una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
