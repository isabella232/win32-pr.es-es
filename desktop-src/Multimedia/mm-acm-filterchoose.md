---
title: Mensaje de MM_ACM_FILTERCHOOSE (MSACM. h)
description: El \_ mensaje mm ACM \_ FILTERCHOOSE notifica a una función de enlace del cuadro de diálogo de acmFilterChoose antes de agregar un elemento a uno de los tres cuadros de lista desplegable.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- Mensaje de MM_ACM_FILTERCHOOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149972"
---
# <a name="mm_acm_filterchoose-message"></a>\_ \_ Mensaje FILTERCHOOSE de mm ACM

El mensaje **mm \_ ACM \_ FILTERCHOOSE** notifica a una función de enlace del cuadro de diálogo de [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) antes de agregar un elemento a uno de los tres cuadros de lista desplegable. Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Cuadro de lista desplegable que se va a inicializar y una operación de comprobación o adición.



| Requisito | Value |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_comprobación personalizada de FILTERCHOOSE \_    | El parámetro *lParam* es un puntero a una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable Nombre personalizado.                                                                                                   |
| FILTERCHOOSE \_ \_ Agregar filtro       | El parámetro *lParam* es un puntero a un búfer que aceptará una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable filtro. La aplicación debe copiar la estructura de filtro que se va a agregar a este búfer. |
| \_comprobación de filtro de FILTERCHOOSE \_    | El parámetro *lParam* es un puntero a una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable filtro.                                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ Add    | El parámetro *lParam* es un puntero a un **valor DWORD** que aceptará una etiqueta de filtro de audio de forma de onda que se va a agregar al cuadro de lista desplegable de etiquetas de filtro.                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ verify | El parámetro *lParam* es una etiqueta de filtro de audio de forma de onda que se mostrará en el cuadro de lista desplegable de etiquetas de filtro.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido por el cuadro de lista especificado en el parámetro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si una aplicación controla este mensaje o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la aplicación procesa la \_ \_ operación agregar filtro FILTERCHOOSE, el tamaño del búfer de memoria proporcionado en *lParam* se determinará a partir de la función [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Si la aplicación procesa una operación de comprobación, la aplicación debe preceder al valor devuelto con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) para evitar que el cuadro de diálogo muestre esta selección o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) para permitir que el cuadro de diálogo muestre esta selección. Si se procesa una operación de agregar, la aplicación debe preceder a la devolución con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) para indicar que no se requieren más adiciones o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) si se requieren más adiciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>MSACM. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de audio](audio-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de audio](audio-compression-messages.md)
</dt> </dl>

 

 





