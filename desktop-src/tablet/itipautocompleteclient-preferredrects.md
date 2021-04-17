---
description: Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: ITipAutocompleteClient::P método referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716587"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient::P método referredRects

Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prcACList* \[ de\]
</dt> <dd>

Rectángulo, en coordenadas de la pantalla, que indica la ubicación preferida del proveedor y el tamaño de la interfaz de usuario de la lista de autocompletar.

</dd> <dt>

*prcField* \[ de\]
</dt> <dd>

Rectángulo, en coordenadas de la pantalla, que indica la ubicación y el tamaño del campo con foco.

</dd> <dt>

*prcModified* \[ enuncia\]
</dt> <dd>

Un rectángulo basado en el estado actual de la sugerencia y la ubicación y el tamaño de la lista de rellenado automático preferidos especificado por *prcACList*.

</dd> <dt>

*pfShownAboveTip* \[ in, out\]
</dt> <dd>

**True** si el rectángulo modificado se va a mostrar sobre el área de destino del panel de entrada de texto; en caso contrario, **false**. Este valor se debe inicializar en la orientación preferida del proveedor antes de que se llame al método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Llame al [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer la ventana Lista de autocompletar emergente antes de llamar al [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Se ha producido un error no especificado.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Este es el método al que el proveedor de autocompletar llama cuando está a punto de mostrar la interfaz de usuario de autocompletar. El cliente modifica el rectángulo preferido del proveedor especificado por *prcACList* a través del argumento *prcModified* .

Llame al [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer el identificador de la ventana Lista de rellenado automático emergente antes de llamar a **PreferredRects**. Si no lo hace, se producirá un error de **E \_ INVALIDARG** al llamar a **PreferredRects**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient:: RequestShowUI (método)**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




