---
description: La manera más sencilla de crear un espacio de nombres es usar Managed Object Format (MOF) para crear el espacio de nombres dentro del directorio actual. El directorio actual se define al iniciar sesión.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Crear un espacio de nombres secundario con código MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d29edf493cb94c92715214dd2d7e7622ae12e831e71322afa8ad590272c6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244645"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Crear un espacio de nombres secundario con código MOF

La manera más sencilla de crear un espacio de nombres es usar Managed Object Format (MOF) para crear el espacio de nombres dentro del directorio actual. El directorio actual se define al iniciar sesión.

En el procedimiento siguiente se describe cómo crear un espacio de nombres secundario mediante código MOF.

**Para crear un espacio de nombres secundario mediante código MOF**

1.  Cree una instancia de la clase [**\_ \_ Namespace.**](--namespace.md)

    En el ejemplo de código siguiente se muestra cómo crear un espacio de nombres secundario.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Si desea exigir al usuario que realice una conexión cifrada al espacio de nombres, use el calificador **RequiresEncryption.** Para obtener más información, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

    En el ejemplo de código siguiente se muestra cómo requerir una conexión cifrada.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Si desea establecer un descriptor de seguridad en el espacio de nombres en lugar de usar la seguridad de espacio de nombres predeterminada, use el calificador **NamespaceSecuritySDDL.** Para obtener más información, vea [Establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).

    En el ejemplo de código siguiente se muestra cómo establecer un descriptor de seguridad en el espacio de nombres .

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Compile y cargue la instancia [**\_ \_ de Namespace**](--namespace.md) mediante la utilidad [mofcomp](mofcomp.md) o [**la interfaz IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) Tanto mofcomp como la **interfaz IMofCompiler** cargan automáticamente el espacio de nombres en el directorio actual. Para obtener más información, [vea Compilar archivos MOF.](compiling-mof-files.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



