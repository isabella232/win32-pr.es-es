---
title: THEME. showErrorDialog
description: El método showErrorDialog muestra el cuadro de diálogo de error estándar.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Media Player de Windows de THEME. showErrorDialog
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690450"
---
# <a name="themeshowerrordialog"></a>THEME. showErrorDialog

El método **showErrorDialog** muestra el cuadro de diálogo de error estándar.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si **Settings. enableErrorDialogs** es false, este método se puede usar para mostrar el cuadro de diálogo de error mediante programación. Si no hay ningún error en la cola de errores, no se muestra el cuadro de diálogo de error.

En Windows Media Player serie 9 o posterior, se debe llamar a este método desde el controlador de eventos de error. Windows Media Player serie 9 o posterior borra la cola de errores de las máscaras una vez que se ha desencadenado el evento de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**Settings. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





