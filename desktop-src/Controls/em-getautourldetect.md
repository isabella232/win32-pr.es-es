---
title: Mensaje EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica si la detección de dirección URL automática está activada en el control Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079457"
---
# <a name="em_getautourldetect-message"></a>\_Mensaje GETAUTOURLDETECT em

Indica si la detección de dirección URL automática está activada en el control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la detección de dirección URL automática está activa, el valor devuelto es 1.

Si la detección de dirección URL automática está inactiva, el valor devuelto es 0.

## <a name="remarks"></a>Observaciones

Cuando la detección de dirección URL automática está activada, Microsoft Rich Edit comprueba constantemente el texto escrito para obtener una dirección URL válida. Rich Edit reconoce las direcciones URL que comienzan con estos prefijos:

-   http:
-   file:
-   mailto:
-   FTP
-   https
-   :/
-   NNTP
-   prospero:
-   habitualmente
-   Reportaje
-   WAIS
-   Outlook

La edición enriquecida también reconoce los nombres de ruta de acceso estándar que comienzan por \\ \\ . Cuando Rich Edit localiza una dirección URL, cambia el color del texto de la dirección URL, subraya el texto y notifica al cliente mediante el [ \_ vínculo en](en-link.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EN \_ vínculo](en-link.md)
</dt> </dl>

 

 





