---
title: THEME.loadPreference
description: El método loadPreference carga una preferencia del Registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME.loadPreference Reproductor de Windows Media
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 252f08c1971b1e8434e3761d87992a7245257c37bcc039650ebf5b7a0a47a884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134578"
---
# <a name="themeloadpreference"></a>THEME.loadPreference

El **método loadPreference** carga una preferencia del Registro.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Cadena **que** especifica la clave del valor de preferencia que se cargará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Comentarios

Una preferencia es un par clave-valor que se puede almacenar en el Registro para conservar información sobre el estado de la Reproductor de Windows Media entre ejecuciones. Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización de modo que no tenga que volver a especificarse cada vez que Reproductor de Windows Media se inicia.

Las preferencias no están cifradas y, por tanto, no son un método seguro para conservar los datos. No use preferencias para almacenar datos privados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**THEME.savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





