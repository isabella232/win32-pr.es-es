---
description: En el ejemplo siguiente, una compañía hipotética de desarrollo de software llamada Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Ejemplo de asociación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad24c3e65ca5b297412c4a69702987cd86b5187dab63dd81435d50e7d06721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009535"
---
# <a name="file-association-example"></a>Ejemplo de asociación de archivos

En el ejemplo siguiente, una compañía hipotética de desarrollo de software llamada Litware, Inc. crea un nuevo reproductor de audio llamado LitwarePlayer. Litware quiere diseñar una asociación de archivos entre LitwarePlayer y su tipo de archivo principal, que usa un formato de audio recién desarrollado que permite almacenar un CD de audio completo en menos de 10 kilobytes de memoria sin pérdida de calidad.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que funcionan las asociaciones de archivos predeterminadas ha cambiado Windows 10. Para obtener más información, vea la sección Sobre los cambios en **Windows 10 controla las aplicaciones predeterminadas** en esta [entrada](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Diseñar una nueva asociación de archivos

La empresa debe realizar los pasos siguientes.

1.  **Decida si el nuevo tipo de archivo debe tratarse como público o privado.** Este nuevo tipo de archivo es un tipo de medio. Dado que los usuarios intercambian archivos multimedia en varias plataformas y puede [](fa-file-types.md) haber otras aplicaciones que necesiten leer el formato LitwarePlayer, un tipo de archivo público es el más adecuado.
2.  **Determine si este tipo de archivo ya está definido.** Compruebe la base de datos MIME de Internet Assigned Numbers Authority (IANA) y otras bases de datos de tipo de archivo público en Internet para determinar que no se ha definido ningún tipo de archivo comparable. Dado que se trata de un nuevo formato de archivo, debe definir un nuevo tipo de archivo.
3.  **Defina una extensión de nombre de archivo para el nuevo tipo de archivo.** Los desarrolladores eligen , que incorpora la abreviatura del proveedor y una `.opa-ltw-audio` sugerencia sobre lo que contiene el archivo. La investigación determina que nadie más usa la extensión. Siguiendo las recomendaciones actuales, no se define ninguna extensión corta.
4.  **Defina un tipo MIME para el tipo de archivo y regístrelo con IANA.** Litware define el nuevo tipo MIME como *audio/LitwarePlayer.1* y prepara una aplicación de tipo MIME, siguiendo las directrices establecidas en los números de solicitud de comentarios (RFC) 2045, 2046, 2047 y 2048. A continuación, envían la aplicación a IANA, que agrega el nuevo tipo de archivo a la base de datos de tipos MIME registrados.
5.  **Determine si existe un ProgID para el tipo de archivo.** Dado que se trata de un nuevo tipo de archivo, no [existe ningún ProgID](fa-progids.md) para él. Litware establece sobre el diseño de un nuevo ProgID para LitwarePlayer. Deciden el nombre descriptivo "LitwarePlayer Audio Player" (que se almacena como un recurso en el archivo LitwarePlayer.exe) y diseñan un icono predeterminado para usarlo para los archivos asociados a LitwarePlayer (también almacenados en LitwarePlayer.exe). Dado que LitwarePlayer es una nueva aplicación, se trata de un ProgID de la versión 1.
6.  **Registre el ProgID.** Cuando se instala LitwarePlayer, el programa de instalación crea la siguiente [entrada ProgID](fa-progids.md) en el Registro.

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

    En la clave de comando, %1 se pasa como ruta de acceso al archivo que se va a reproducir.

7.  **Registre la extensión de nombre de archivo para el tipo de archivo.** Cuando se instala LitwarePlayer, el programa de instalación crea las siguientes entradas en el Registro para su extensión de tipo de archivo personalizado.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Siempre que se cree o cambie una asociación de archivos, notifique al sistema que se ha realizado un cambio mediante una llamada a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el evento \_ ASSOCCHANGED de SHCNE. Si esto no se hace, es posible que el Shell no reconozca los cambios realizados hasta que se reinicie el sistema.

 

## <a name="additional-resources"></a>Recursos adicionales

-   [Introducción a las asociaciones de archivos](fa-intro.md)
-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el Windows inicio](start-menu-reg.md)
-   [Registro de una aplicación en un esquema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Establecer el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
