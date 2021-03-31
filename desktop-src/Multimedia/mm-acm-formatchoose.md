---
title: Mensaje de MM_ACM_FORMATCHOOSE (MSACM. h)
description: El \_ mensaje FORMATCHOOSE de mm ACM \_ notifica a una función de enlace del cuadro de diálogo acmFormatChoose antes de agregar un elemento a uno de los tres cuadros de lista desplegable.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- Mensaje de MM_ACM_FORMATCHOOSE de Windows multimedia
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
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804093"
---
# <a name="mm_acm_formatchoose-message"></a>\_ \_ Mensaje FORMATCHOOSE de mm ACM

El **mensaje \_ \_ FORMATCHOOSE de mm ACM** notifica a una función de enlace del cuadro de diálogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) antes de agregar un elemento a uno de los tres cuadros de lista desplegable. Este mensaje permite a una aplicación personalizar aún más las selecciones disponibles a través de la interfaz de usuario.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Cuadro de lista desplegable que se va a inicializar y una operación de comprobación o adición.



| Requisito | Value |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_comprobación personalizada de FORMATCHOOSE \_    | El parámetro *lParam* es un puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable Nombre personalizado.                                                                                                   |
| \_Agregar formato \_ FORMATCHOOSE       | El parámetro *lParam* es un puntero a un búfer que aceptará una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable formato. La aplicación debe copiar la estructura de formato que se va a agregar a este búfer. |
| \_comprobación de formato de FORMATCHOOSE \_    | El parámetro *lParam* es un puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que se va a agregar al cuadro de lista desplegable formato.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ Add    | El parámetro *lParam* es un puntero a una variable que aceptará una etiqueta de formato de audio de forma de onda que se va a agregar al cuadro de lista desplegable de etiqueta de formato.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ verify | El parámetro *lParam* es una etiqueta de formato de audio de forma de onda que se mostrará en el cuadro de lista desplegable formato de etiqueta.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valor definido por el cuadro de lista especificado en el parámetro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si una aplicación controla este mensaje o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la aplicación procesa la \_ operación de \_ Agregar formato FILTERCHOOSE, el tamaño del búfer de memoria proporcionado en *lParam* se determinará a partir de la función [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Si la aplicación está procesando una operación de comprobación, puede impedir que el cuadro de diálogo muestre esta selección mediante una llamada a la función **SetWindowLong** con *NINDEX* establecida en DWL \_ MSGRESULT y *lNewLong* establecida en **false** (convertir a un tipo de datos **Long** ). Para permitir que el cuadro de diálogo muestre esta selección, llame a esta función con *lNewLong* establecido en **true**.

Si la aplicación está procesando una operación de agregar, puede indicar que no se requieren más adiciones mediante una llamada a la función **SetWindowLong** con *NINDEX* establecida en DWL \_ MSGRESULT y *lNewLong* establecida en **false** (convertir a un tipo de datos **Long** ). Para indicar que se necesitan más adiciones, llame a esta función con *lNewLong* establecido en **true**.

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

 

