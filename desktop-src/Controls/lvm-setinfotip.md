---
title: Mensaje de LVM_SETINFOTIP (commctrl. h)
description: Establece el texto de información sobre herramientas en respuesta diferida en la notificación de GETINFOTIP de LVN \_ .
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656467"
---
# <a name="lvm_setinfotip-message"></a>\_Mensaje SETINFOTIP LVM

Establece el texto de información sobre herramientas en respuesta diferida en la notificación de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> que contiene la información que se va a establecer.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el texto de información sobre herramientas se establece correctamente, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El mensaje **LVM \_ SETINFOTIP** permite a una aplicación calcular recuadros informativos en segundo plano realizando los pasos siguientes:

1.  En respuesta a la notificación de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) , establezca el miembro **miembros pszText** de la estructura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) en una cadena vacía y devuelva 0.
2.  En segundo plano, calcule el recuadro informativo.
3.  Después de calcular el recuadro informativo, envíe el mensaje **LVM \_ SETINFOTIP** , estableciendo el miembro **miembros pszText** de la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) en el elemento recuadro informativo y los miembros **iItem** y **iSubItem** en el elemento y el subelemento al que se aplica el recuadro informativo.

El texto que se pasa al mensaje **LVM \_ SETINFOTIP** solo aparece si el elemento y el subelemento descritos por la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) siguen en un estado que requiere un recuadro informativo

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





