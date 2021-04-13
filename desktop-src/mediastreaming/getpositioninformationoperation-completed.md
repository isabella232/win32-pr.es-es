---
title: Propiedad GetPositionInformationOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetPositionInformationAsync.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz GetPositionInformationOperation
- Interfaz GetPositionInformationOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420681"
---
# <a name="getpositioninformationoperationcompleted-property"></a>Propiedad GetPositionInformationOperation. Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) .

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

 