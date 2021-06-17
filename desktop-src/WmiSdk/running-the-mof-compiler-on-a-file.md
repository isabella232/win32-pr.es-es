---
description: 'Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ejecución del compilador MOF en un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230242"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Ejecución del compilador MOF en un archivo

Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.

Hasta que ejecute el compilador MOF, [**Mofcomp.exe**](mofcomp.md), un proveedor no está registrado con WMI y las clases que creó en el archivo MOF no están disponibles en el [*repositorio WMI*](gloss-w.md). En el procedimiento siguiente se describe cómo compilar un archivo MOF.

**Para ejecutar el compilador MOF en un archivo desde la línea de comandos**

1.  Llame al compilador MOF desde la línea de comandos con la sintaxis siguiente.

    **mofcomp** _MOFfile_**.mof**

    El compilador de MOF admite una variedad de modificadores para controlar situaciones de procesamiento especiales. Todos los modificadores son opcionales y se permite cualquier combinación de modificadores. Sin embargo, no tiene sentido usar algunos de los modificadores en combinación con otros. Por ejemplo, para combinar los modificadores **-class:updateonly** y **-class:createonly,** el compilador no realiza ninguna acción.

    De forma predeterminada, Mofcomp.exe las clases compiladas en el espacio de \\ nombres WMI predeterminado raíz. Tenga en cuenta que el espacio de nombres predeterminado Mofcomp.exe no es el mismo que el espacio de nombres predeterminado para scripting. El espacio de nombres predeterminado para scripting se especifica en el Control WMI de la pestaña Opciones avanzadas. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

    Puede cambiar el espacio de nombres que recibe las clases de dos maneras.

    1.  Use el **modificador -N** para el **comando mofcomp.**
    2.  Inserte el espacio de nombres \# [**pragma del comando de preprocesador**](pragma-namespace.md) en el archivo MOF.

2.  Opcionalmente, puede compilar un archivo MOF mediante programación. Para obtener más información, [**vea IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilación de archivos MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



