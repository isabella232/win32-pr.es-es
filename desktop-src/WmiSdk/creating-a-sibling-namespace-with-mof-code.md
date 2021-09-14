---
description: Otra manera de crear un espacio de nombres es usar Managed Object Format (MOF) para crear un espacio de nombres relacionado. Un espacio de nombres relacionado es un espacio de nombres que no existe como elemento secundario del espacio de nombres actual.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Crear un espacio de nombres relacionado con código MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170501"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>Crear un espacio de nombres relacionado con código MOF

Otra manera de crear un espacio de nombres es usar Managed Object Format (MOF) para crear un espacio de nombres relacionado. Un espacio de nombres relacionado es un espacio de nombres que no existe como elemento secundario del espacio de nombres actual.

En el procedimiento siguiente se describe cómo crear un espacio de nombres relacionado con código MOF.

**Para crear un espacio de nombres relacionado con código MOF**

1.  Inserte el [**\# comando pragma namespace**](pragma-namespace.md) en el código MOF antes de la declaración del espacio de nombres.

    El [**\# comando pragma namespace**](pragma-namespace.md) indica a WMI dónde crear las instancias siguiendo la directiva .

2.  Cree una instancia de la clase [**\_ \_ Namespace.**](--namespace.md)
3.  Compile el código con [la utilidad mofcomp](mofcomp.md) o la [**interfaz IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Para obtener más información, [vea Compilar archivos MOF.](compiling-mof-files.md)

En el siguiente ejemplo de código MOF se describe cómo crear un espacio de nombres como un elemento relacionado con el espacio de nombres \\ "ROOT CIMv2".

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



