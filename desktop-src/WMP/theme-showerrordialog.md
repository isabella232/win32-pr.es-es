---
title: THEME.showErrorDialog
description: El método showErrorDialog muestra el cuadro de diálogo de error estándar.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEME.showErrorDialog Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168602"
---
# <a name="themeshowerrordialog"></a>THEME.showErrorDialog

El **método showErrorDialog** muestra el cuadro de diálogo de error estándar.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si **Configuración.enableErrorDialogs** es false, este método se puede usar para mostrar mediante programación el cuadro de diálogo de error. Si no hay errores en la cola de errores, no se muestra el cuadro de diálogo de error.

Para Reproductor de Windows Media serie 9 o posterior, se debe llamar a este método desde el controlador de eventos de error. Reproductor de Windows Media serie 9 o posterior borra la cola de errores para las máscaras después de que se haya desencadenado el evento de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> <dt>

[**Configuración.enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





