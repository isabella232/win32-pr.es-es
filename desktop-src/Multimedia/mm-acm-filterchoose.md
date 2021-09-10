---
title: MM_ACM_FILTERCHOOSE mensaje (Msacm.h)
description: El mensaje MM ACM FILTERCHOOSE notifica a una función de enlace de cuadro de diálogo \_ acmFilterChoose antes de agregar un elemento a uno de los tres cuadros de \_ lista desplegable.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370315"
---
# <a name="mm_acm_filterchoose-message"></a>Mensaje \_ DE MM ACM \_ FILTERCHOOSE

El **mensaje MM \_ ACM \_ FILTERCHOOSE** notifica a una función de enlace de cuadro de diálogo [**acmFilterChoose antes**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) de agregar un elemento a uno de los tres cuadros de lista desplegable. Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Cuadro de lista desplegable que se inicializa y una operación de comprobación o adición.



| Requisito | Value |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTERCHOOSE \_ CUSTOM \_ VERIFY    | El *parámetro lParam* es un puntero a una [**estructura WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable Nombre personalizado.                                                                                                   |
| FILTERCHOOSE \_ FILTER \_ ADD       | El *parámetro lParam* es un puntero a un búfer que aceptará una estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable Filtro. La aplicación debe copiar la estructura de filtro que se va a agregar a este búfer. |
| FILTERCHOOSE \_ FILTER \_ VERIFY    | El *parámetro lParam* es un puntero a una [**estructura WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) que se va a agregar al cuadro de lista desplegable Filtro.                                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ ADD    | El *parámetro lParam* es un puntero a **un DWORD** que aceptará una etiqueta de filtro de audio de forma de onda que se agregará al cuadro de lista desplegable Etiqueta de filtro.                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ VERIFY | El *parámetro lParam es* una etiqueta de filtro de audio de forma de onda que se mostrará en el cuadro de lista desplegable Etiqueta de filtro.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido por el cuadro de lista especificado en el **parámetro wParam.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** una aplicación controla este mensaje o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Si la aplicación procesa la operación FILTERCHOOSE FILTER ADD, el tamaño del búfer de memoria proporcionado en lParam se determinará a partir de la \_ \_ función [**acmMetrics.**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 

Si la aplicación procesa una operación de comprobación, la aplicación debe preceder el valor devuelto con **SetWindowLong** (hwnd, DWL MSGRESULT, (LONG) FALSE ) para evitar que el cuadro de diálogo enumere esta selección o con \_ **SetWindowLong** (hwnd, DWL  \_ MSGRESULT, (LONG)**TRUE)** para permitir que el cuadro de diálogo enumere esta selección. Si procesa una operación de adición, la aplicación debe preceder a la devolución con **SetWindowLong** (hwnd, DWL MSGRESULT, (LONG) FALSE ) para indicar que no se requieren más adiciones o con \_ **SetWindowLong** (hwnd, DWL \_ MSGRESULT, (LONG)**TRUE)** si se requieren más adiciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





