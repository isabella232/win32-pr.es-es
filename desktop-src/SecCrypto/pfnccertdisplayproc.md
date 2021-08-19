---
description: Función de devolución de llamada definida por el usuario que permite al autor de la llamada de la función CryptUIDlgSelectCertificate controlar la presentación de los certificados que el usuario selecciona para ver.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Función de devolución de llamada PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978981"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Función de devolución de llamada PFNCCERTDISPLAYPROC

La **función PFNCCERTDISPLAYPROC** es una función de devolución de llamada definida por el usuario que permite al autor de la llamada de la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) controlar la presentación de los certificados que el usuario selecciona para ver.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCertContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado que se muestra.

</dd> <dt>

*hWndSelCertDlg* \[ En\]
</dt> <dd>

Identificador del cuadro de diálogo desde el que se seleccionó el certificado para su visualización.

</dd> <dt>

*pvCallbackData* \[ En\]
</dt> <dd>

Datos adicionales usados por la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE para** indicar que controla la presentación del certificado y que el cuadro de diálogo no debe mostrar el certificado. Si esta función devuelve **FALSE**, el cuadro de diálogo muestra el certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 




