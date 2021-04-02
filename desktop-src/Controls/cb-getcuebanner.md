---
title: Mensaje de CB_GETCUEBANNER (Winuser. h)
description: Obtiene el texto del titular de indicación mostrado en el control de edición de un cuadro combinado. Envíe este mensaje explícitamente o mediante la \_ macro GetCueBannerText de ComboBox.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905369"
---
# <a name="cb_getcuebanner-message"></a>\_Mensaje GETCUEBANNER CB

Obtiene el texto del titular de indicación mostrado en el control de edición de un cuadro combinado. Envíe este mensaje explícitamente o mediante la [**macro \_ GetCueBannerText de ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Un puntero a un búfer de cadena Unicode que recibe el texto del titular de indicación. La aplicación que realiza la llamada es responsable de asignar la memoria para el búfer. El tamaño del búfer debe ser igual a la longitud de la cadena de banner de indicación en **WCHARs**, además de 1 para el **WCHAR** **nulo** de terminación.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta *lpcwText* en **WCHARs**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente, o un valor de error en caso contrario.

Si no hay ningún texto de titular de indicación para obtener, el valor devuelto es 0. Si la aplicación que realiza la llamada no puede asignar un búfer o establece *lParam* antes de enviar este mensaje, podría producirse un comportamiento indefinido y es posible que el valor devuelto no sea confiable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





