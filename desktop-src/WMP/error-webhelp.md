---
title: Error. WebHelp (método)
description: El método WebHelp inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero). | Error. WebHelp (método)
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- método WebHelp Windows Media Player
- método WebHelp Windows Media Player, clase error
- Clase de error Windows Media Player, método WebHelp
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
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700108"
---
# <a name="errorwebhelp-method"></a>Error. WebHelp (método)

El método **WebHelp** inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero).

## <a name="syntax"></a>Sintaxis


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las páginas de ayuda web siempre contienen la información más reciente y más detallada sobre los errores de Windows Media Player. Este método transfiere automáticamente la otra información que necesita la ayuda Web, como la versión del sistema operativo que se está usando.

Para tener acceso directamente a las páginas de ayuda Web, use el código de error y los vínculos del centro de soporte técnico siguientes.

-   [Información del código de error de Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro de soluciones de Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación deseada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que inicia la página de ayuda Web de Microsoft Windows Media Player. El objeto **Player** se creó con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> </dl>

 

 





