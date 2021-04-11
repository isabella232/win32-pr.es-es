---
description: 'Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ejecutar el compilador MOF en un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276142"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Ejecutar el compilador MOF en un archivo

Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.

Hasta que ejecute el compilador MOF, [**Mofcomp.exe**](mofcomp.md), un proveedor no se registra con WMI y las clases que creó en el archivo MOF no están disponibles en el [*repositorio WMI*](gloss-w.md). En el procedimiento siguiente se describe cómo compilar un archivo MOF.

**Para ejecutar el compilador MOF en un archivo desde la línea de comandos**

1.  Llame al compilador MOF desde la línea de comandos con la siguiente sintaxis.

    **MOFCOMP** *MOFfile * * *. mof**

    El compilador MOF admite diversos modificadores para controlar situaciones de procesamiento especiales. Todos los modificadores son opcionales y se permite cualquier combinación de modificadores. Sin embargo, no tiene sentido usar algunos de los conmutadores en combinación con otros. Por ejemplo, para combinar los modificadores **-Class: updateonly** y **-Class: createonly** , el compilador no realiza ninguna acción.

    De forma predeterminada, Mofcomp.exe almacena las clases compiladas en el \\ espacio de nombres WMI predeterminado raíz. Tenga en cuenta que el espacio de nombres predeterminado para Mofcomp.exe no es el mismo que el espacio de nombres predeterminado para scripting. El espacio de nombres predeterminado para scripting se especifica en el control WMI en la pestaña Opciones avanzadas. Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

    Puede cambiar el espacio de nombres que recibe las clases de dos maneras.

    1.  Use el modificador **-N** para el comando **MOFCOMP** .
    2.  Inserte el \# [**espacio de nombres pragma**](pragma-namespace.md) Command de preprocesador en el archivo MOF.

2.  Opcionalmente, puede compilar un archivo MOF mediante programación. Para obtener más información, vea [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar archivos MOF](compiling-mof-files.md)
</dt> <dt>

[**MOFCOMP**](mofcomp.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



