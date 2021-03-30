---
description: Función de devolución de llamada definida por el usuario que permite al llamador de la función CryptUIDlgSelectCertificate controlar la presentación de los certificados que el usuario selecciona para su visualización.
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
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082709"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Función de devolución de llamada PFNCCERTDISPLAYPROC

La función **PFNCCERTDISPLAYPROC** es una función de devolución de llamada definida por el usuario que permite al autor de la llamada de la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) controlar la presentación de los certificados que el usuario selecciona para verlos.

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

*pCertContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado que se va a mostrar.

</dd> <dt>

*hWndSelCertDlg* \[ de\]
</dt> <dd>

Identificador del cuadro de diálogo del que se seleccionó el certificado para su visualización.

</dd> <dt>

*pvCallbackData* \[ de\]
</dt> <dd>

Datos adicionales usados por la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** para indicar que controla la presentación del certificado y que el cuadro de diálogo no debe mostrar el certificado. Si esta función devuelve **false**, el cuadro de diálogo muestra el certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 




