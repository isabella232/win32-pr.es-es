---
title: Propiedad PublicMode de IMsRdpClientShell
description: Especifica o recupera si el modo público está habilitado.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Propiedad PublicMode Servicios de Escritorio remoto
- Propiedad PublicMode Servicios de Escritorio remoto , interfaz IMsRdpClientShell
- Interfaz IMsRdpClientShell Servicios de Escritorio remoto , propiedad PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a8594d69810b144dbea51c33d8044215dd8d603eee6dd315f624a2f942720a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854479"
---
# <a name="imsrdpclientshellpublicmode-property"></a>IMsRdpClientShell::P ublicMode

Especifica o recupera si el modo público está habilitado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si el modo público está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClientShell se define como \_ d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





