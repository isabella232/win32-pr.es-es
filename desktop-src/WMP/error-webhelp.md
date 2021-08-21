---
title: Método Error.webHelp
description: El método webHelp inicia la página Reproductor de Windows Media Web Help para mostrar más información sobre el primer error en la cola de errores (índice cero). | Método Error.webHelp
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Método webHelp Reproductor de Windows Media
- método webHelp Reproductor de Windows Media , Clase Error
- Clase de error Reproductor de Windows Media , método webHelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577879"
---
# <a name="errorwebhelp-method"></a>Método Error.webHelp

El **método webHelp** inicia la página Reproductor de Windows Media Web Help para mostrar más información sobre el primer error en la cola de errores (índice cero).

## <a name="syntax"></a>Sintaxis


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las páginas de Ayuda web siempre contienen la información más reciente y más detallada sobre Reproductor de Windows Media errores. Este método transfiere automáticamente la otra información necesaria para la Ayuda web, como la versión del sistema operativo que se usa.

Para acceder directamente a las páginas de Ayuda web, use el código de error siguiente y los vínculos del Centro de soporte técnico.

-   [Reproductor de Windows Media Información del código de error](https://support.microsoft.com/kb/886273)
-   [Reproductor de Windows Media Centro de soluciones](https://support.microsoft.com/ph/7763#tab0)

**Reproductor de Windows Media 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación prevista.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que inicia la página microsoft Reproductor de Windows Media Web Help. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> </dl>

 

 





