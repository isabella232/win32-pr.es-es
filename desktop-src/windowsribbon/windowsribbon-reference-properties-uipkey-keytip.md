---
title: UI_PKEY_Keytip
description: Identifica la \_ propiedad KeyTip PKEY de la interfaz de usuario \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994295"
---
# <a name="ui_pkey_keytip"></a>KeyTip de UI \_ PKEY \_

Identifica la \_ propiedad KeyTip PKEY de la interfaz de usuario \_ .

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa KeyTip de PKEY de IU para consultar la tecla de aceleración de un control de la cinta de opciones.

Este valor de propiedad es una cadena, que se compone de cualquier secuencia de caracteres, incluido el espacio en blanco.

El valor de KeyTip de UI \_ PKEY \_ actúa como la tecla de aceleración para un comando, a menos que ese comando se exponga a través de un elemento de menú. En este caso, el marco de trabajo omite el valor de KeyTip PKEY de la interfaz de usuario \_ \_ y, en su lugar, usa un carácter precedido por una y comercial según lo especificado por el [**comando. LabelTitle**](windowsribbon-element-command-labeltitle.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario. Si no se especifica el carácter de y comercial mediante la etiqueta **Command. LabelTitle** o UI \_ PKEY \_ , no se expone ningún KeyTip ni tecla de aceleración.

La longitud máxima de KeyTip de PKEY de la interfaz de usuario \_ \_ no está enlazada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de recursos](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. KeyTip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




