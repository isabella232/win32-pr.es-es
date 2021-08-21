---
title: TTM_SETTITLE mensaje (Commctrl.h)
description: Agrega un icono estándar y una cadena de título a una información sobre herramientas.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e159ce522ea27361f93beaa96da06959fba6f92fedf5981dfd049ddc7f36cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166358"
---
# <a name="ttm_settitle-message"></a>Mensaje \_ SETTITLE de TTM

Agrega un icono estándar y una cadena de título a una información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establezca *wParam en* uno de los siguientes valores para especificar el icono que se va a mostrar. A Windows XP SP2 y versiones posteriores, este parámetro también puede contener un **valor HICON.** Se supone que cualquier valor mayor que TTI \_ ERROR es **hicon.**



| Valor                                                                                                                                                                      | Significado                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ NONE**</dt> </dl>                             | Sin icono.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**INFORMACIÓN \_ DE TTI**</dt> </dl>                             | Icono de información.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**ADVERTENCIA \_ DE TTI**</dt> </dl>                    | Icono de advertencia<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**ERROR \_ DE TTI**</dt> </dl>                          | Icono de error<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ INFO \_ LARGE**</dt> </dl>          | Icono de error grande<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**ADVERTENCIA DE TTI \_ \_ GRANDE**</dt> </dl> | Icono de error grande<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**ERROR DE TTI \_ \_ GRANDE**</dt> </dl>       | Icono de error grande<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena de título. Debe asignar un valor a *lParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente, FALSE** si no es así.

## <a name="remarks"></a>Comentarios

El título de una información sobre herramientas aparece encima del texto, en una fuente diferente. No es suficiente tener un título; la información sobre herramientas también debe tener texto o no se muestra.

Cuando *wParam contiene* un **HICON,** la ventana de información sobre herramientas crea una copia del icono.

Al llamar **a TTM \_ SETTITLE**, la cadena a la que apunta *lParam* no debe superar los 100 **TCHAR** de longitud, incluido el **valor NULL final.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo agregar un título y un icono del sistema a una información sobre herramientas.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ SETTITLEW** (Unicode) y **TTM \_ SETTITLEA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles de información sobre herramientas](tooltip-controls.md)
</dt> </dl>

 

 





