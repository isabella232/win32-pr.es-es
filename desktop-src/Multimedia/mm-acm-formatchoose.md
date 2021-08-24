---
title: MM_ACM_FORMATCHOOSE mensaje (Msacm.h)
description: El mensaje FORMATCHOOSE de MM ACM notifica a una función de enlace de diálogo \_ acmFormatChoose antes de agregar un elemento a uno de los tres cuadros \_ de lista desplegable.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceaa67bc0ce4ee922b48d1cff20eb2bf6414f93506dcc70ccd6e0e912211544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782965"
---
# <a name="mm_acm_formatchoose-message"></a>Mm \_ ACM \_ FORMATCHOOSE message

El **mensaje \_ \_ FORMATCHOOSE** de MM ACM notifica a una función de enlace de diálogo [**acmFormatChoose antes**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) de agregar un elemento a uno de los tres cuadros de lista desplegable. Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Cuadro de lista desplegable que se inicializa y una operación de comprobación o adición.



| Requisito | Valor |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATCHOOSE \_ CUSTOM \_ VERIFY    | El *parámetro lParam es* un puntero a una estructura [**DESACMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable Nombre personalizado.                                                                                                   |
| FORMATCHOOSE \_ FORMAT \_ ADD       | El *parámetro lParam* es un puntero a un búfer que aceptará una estructura [**DESATEX que**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) se va a agregar al cuadro de lista desplegable Formato. La aplicación debe copiar la estructura de formato que se va a agregar a este búfer. |
| FORMATCHOOSE \_ FORMAT \_ VERIFY    | El *parámetro lParam* es un puntero a una estructura [**DE FORMA DESATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable Formato.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ ADD    | El *parámetro lParam* es un puntero a una variable que aceptará una etiqueta de formato de audio de forma de onda que se va a agregar al cuadro de lista desplegable Etiqueta de formato.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ VERIFY | El *parámetro lParam es* una etiqueta de formato de audio de forma de onda que se mostrará en el cuadro de lista desplegable Etiqueta de formato.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido por el cuadro de lista especificado en el **parámetro wParam.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** una aplicación controla este mensaje o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Si la aplicación procesa la operación FILTERCHOOSE FORMAT ADD, el tamaño del búfer de memoria proporcionado en lParam se determinará a partir de la \_ \_ función [**acmMetrics.**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 

Si la aplicación está procesando una operación de comprobación, puede impedir que el cuadro de diálogo presente esta selección llamando a la función **SetWindowLong** con *nIndex* establecido en DWL MSGRESULT y \_ *lNewLong* establecido en **FALSE** (convertido a un tipo de datos **LONG).** Para permitir que el cuadro de diálogo enume esta selección, llame a esta función con *lNewLong* establecido en **TRUE.**

Si la aplicación está procesando una operación de adición, puede indicar que no se necesitan más adiciones llamando a la función **SetWindowLong** con *nIndex* establecido en DWL MSGRESULT y \_ *lNewLong* establecido en **FALSE** (convertido a un tipo de datos **LONG).** Para indicar que se requieren más adiciones, llame a esta función con *lNewLong* establecido en **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Msacm.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de audio](audio-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de audio](audio-compression-messages.md)
</dt> </dl>

 

