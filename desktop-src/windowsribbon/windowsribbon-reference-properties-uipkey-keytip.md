---
title: UI_PKEY_Keytip
description: Identifica la propiedad \_ IU PKEY \_ Keytip.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028613"
---
# <a name="ui_pkey_keytip"></a>Información sobre \_ claves PKEY \_ de la interfaz de usuario

Identifica la propiedad \_ IU PKEY \_ Keytip.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentarios

Una aplicación usa la información sobre teclas PKEY de la interfaz de usuario \_ para consultar el acelerador de teclado de un control de cinta de \_ opciones.

Este valor de propiedad es una cadena, compuesta de cualquier secuencia de caracteres, incluido el espacio en blanco.

El valor de IU PKEY Keytip actúa como acelerador de teclado para un comando a menos que ese comando \_ \_ se exponga a través de un elemento de menú. En este caso, el marco omite el valor de keytip PKEY de la interfaz de usuario y, en su lugar, usa un carácter precedido por una y comercial, tal y como se especifica en \_ \_ [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o ui [ \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Si no se especifica ninguna yand mediante **Command.LabelTitle** o UI PKEY Label, no se expone ninguna tecla o acelerador \_ \_ de teclado.

La longitud máxima de la información sobre claves PKEY de la interfaz de \_ usuario está sin \_ enlazar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.Keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




